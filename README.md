Mysql

表	字段	操作	说明
fx_construction_team	bank_account	添加	银行账户
opening_bank	添加	开户行
total_applied_amount	添加	总申请金额
actual_paid_amount	添加	总已付
fx_budget_technique	type	添加	类别（1-普通工艺，2-补差工艺）
fx_project	basis_decorate_price	添加	基装总额
applied_material_price	添加	已申请辅材价格
applied_labour_price	添加	已申请人工价格
demolition_budget_rate	添加	拆除预算百分比
basis_hard_rate	添加	基础硬装百分比
basis_compensation_rate	添加	基装补差百分比
suggest_basis_ratio	添加	建议基装总额比例
fx_project_technique	所有	添加	项目补差工艺表
fx_project_visa_technique	所有	添加	项目变更工艺表
fx_workflow_template	unit_base_price	添加	硬装套餐单价
management_rate	添加	施工管理费率
profit_rate	添加	利润率
tax_rate	添加	税率
demolition_budget_rate	添加	拆除预算百分比
basis_hard_rate	添加	基础硬装百分比
basis_compensation_rate	添加	基装补差百分比
suggest_basis_ratio	添加	建议基装总额比例
fx_construction_team_payment	所有	添加	劳务付款表

Redis

表	操作	说明
serial_number:audit_labour	添加	人工申请的编号
instantiate_value:audit_labour_technique:budget_technique	添加	人工申请工艺项实例化工艺信息
field_name:audit_labour	添加	人工申请补充字段
field_name:construction_team_payment	添加	劳务付款补充字段
field_name:project_technique	添加	项目补差工艺补充字段
field_name:project_visa_technique	添加	项目变更工艺补充字段

问题：


额外说明：

预算和拆除预算在完成实例化时要将工艺类别数据也实例化
材料清单的基装辅材如果没下单的可以修改其它属性和删除，材料清单的基装辅材的其它属性只有新增的产品可以编辑属性和删除
预算和拆除预算完成时要更新项目的基装总额
人工申请时添加工艺项的列表需要加上价格，M用1算

上线:

budget_technique的type全部默认为1
