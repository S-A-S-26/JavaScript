# JavaScript
Used Commands

## Using Delegation to get element 
```document.addEventListener('click', function(event) {
						if (event.target.matches('input[data-fieldname="allow_edit"][type="checkbox"]')) {
							console.log("Checkbox clicked",event);
							console.log("event.chekced",event.target.checked)
							var row = event.target.closest('.grid-row');
							if (event.target.checked){
								if (row) {
									var rowDataName = row.getAttribute('data-name');
									var rowDataIdx = row.getAttribute('data-idx');
									console.log("Row data-name:", rowDataName);
									console.log("Row data-idx:", rowDataIdx);
									// Add your logic here
									let sel1=row.querySelector('select[data-fieldname="first_half_of_day"][type="text"]')
									let div1=row.querySelector('select[data-fieldname="first_half_of_day"][data-fieldtype="Select"]')
									console.log("sel1 true",sel1)
									console.log("div1",div1)
									div1.style.visibility="hidden"
									sel1.readOnly=true
								}
								
							}else{
								let sel1=row.querySelector('select[data-fieldname="first_half_of_day"][type="text"]')
								console.log("sel1 false",sel1)
								sel1.readOnly=false
								let div1=row.querySelector('select[data-fieldname="first_half_of_day"][data-fieldtype="Select"]')
								console.log("div1",div1)
								div1.style.visibility="visible"
							}
							// Add your checkbox click event logic here
						}
					});```
