---
description: Você pode usar os métodos do objeto SWbemLocator para obter um objeto SWbemServices que representa uma conexão com um namespace em um computador local ou em um computador host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objeto SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813340"
---
# <a name="swbemlocator-object"></a>Objeto SWbemLocator

Você pode usar os métodos do objeto **SWbemLocator** para obter um objeto [**SWbemServices**](swbemservices.md) que representa uma conexão com um namespace em um computador local ou em um computador host remoto. Em seguida, você pode usar os métodos do objeto **SWbemServices** para acessar o WMI. Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .

## <a name="members"></a>Membros

O objeto **SWbemLocator** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemLocator** tem esses métodos.



| Método                                              | Descrição                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Conecta-se ao WMI no computador especificado.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemLocator** tem essas propriedades.



| Propriedade                                                | Tipo de acesso          | Descrição                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Segurança\_**](swbemlocator-security-.md)<br/> | Somente leitura<br/> | Usado para ler ou alterar as configurações de segurança.<br/> |



 

## <a name="remarks"></a>Comentários

Na parte superior do modelo de objeto da biblioteca de scripts do WMI está o objeto SWbemLocator. SWbemLocator é usado para estabelecer uma conexão autenticada com um namespace WMI, assim como a função VBScript GetObject e o moniker WMI "winmgmts:" são usados para estabelecer uma conexão autenticada com o WMI. No entanto, o SWbemLocator foi projetado para abordar dois cenários de script específicos que não podem ser executados usando GetObject e o moniker WMI. Você deve usar SWbemLocator se precisar:

-   Forneça credenciais de usuário e senha para se conectar ao WMI em um computador remoto. O moniker WMI usado com a função GetObject não inclui um mecanismo para especificar credenciais. A maioria das atividades do WMI (incluindo todas as que são executadas em computadores remotos) exige direitos de administrador. Se você normalmente faz logon usando uma conta de usuário comum em vez de uma conta de administrador, não poderá executar a maioria das tarefas do WMI, a menos que execute o script em credenciais alternativas.
-   Conecte-se ao WMI se você estiver executando um script WMI de dentro de uma página da Web. Você não pode usar a função GetObject ao executar scripts inseridos em uma página HTML porque o Internet Explorer não permite o uso de GetObject por motivos de segurança.

Além disso, talvez você queira usar o SWbemLocator para se conectar ao WMI se encontrar a cadeia de conexão do WMI usada com GetObject confuso ou difícil.

Você usa CreateObject em vez de GetObject para criar uma referência a SWbemLocator. Para criar a referência, você deve passar a função CreateObject do identificador programático SWbemLocator (ProgID) "WbemScripting. SWbemLocator", conforme mostrado na linha 2 no exemplo de script a seguir. Depois de obter uma referência a um objeto SWbemLocator, você chama o método ConnectServer para se conectar ao WMI e obter uma referência a um objeto SWbemServices. Isso é demonstrado na linha 3 do script a seguir.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Para executar um script em credenciais alternativas, inclua o nome de usuário e a senha como parâmetros adicionais passados para ConnectServer. Por exemplo, esse script é executado sob as credenciais de um usuário chamado kenmyer, com a senha homerj.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Você também pode usar o formato de nome de usuário de domínio \\ para especificar um nome de usuário. Por exemplo:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Exemplos

O exemplo do PowerShell a seguir usa **SWbemLocator** para se conectar a um servidor.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | ISWbemLocator de IID \_<br/>                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




