Syntax
irctc.pnrstatus pnr ⟦text⟧
Description
This command checks the pnr status of user's booking on irctc .

Argument	Type	Required	Default Value	Description
pnr	text	yes		Enter the pnr number
result	text	no	heartsresult	Name of a variable where the command's result will be stored
if	bool	no	true	Executes the command only if a specified condition is true
timeout	timespan	no	heartstimeoutcommand	Specifies time in milliseconds for G1ANT.Robot to wait for the command to be executed
errorcall	procedure	no		Name of a procedure to call when the command throws an exception or when a given timeout expires
errorjump	label	no		Name of the label to jump to when the command throws an exception or when a given timeout expires
errormessage	text	no		A message that will be shown in case the command throws an exception or when a given timeout expires, and no errorjump argument is specified
errorresult	variable	no		Name of a variable that will store the returned exception. The variable will be of error structure
For more information about if, timeout, errorcall, errorjump, errormessage and errorresult arguments, see Common Arguments page.

Example
This simple script open IRCTC in chrome and then check the status for given pnr.

irctc.open Type ‴chrome‴ 
delay 10
irctc.pnrstatus pnr ‴1234567890‴ 
