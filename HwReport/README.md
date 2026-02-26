A playbook to report arbitrary data from server facts in a CSV file. 

The playbook calculates variables, either for ansible_facts or for whatever specific data you need, like installed applications, free resources or anything, and the last tasks in the playbook render the template.

To extend, only calculate new variables in the playbook and add them in a row to the CSV template. The template has some black magic in the form of jinja macros so that the CSV is escaped with quotes and can take escaped quotes in any field.
## usage

`ansible-playbook -i inventory report_hw_characteristics.yml --skip-tags=transfer`

