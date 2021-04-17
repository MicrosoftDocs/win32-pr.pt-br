---
description: 'A classe do provedor de registro do sistema StdRegProv para WMI tem métodos que fazem o seguinte:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Alterar dados de Registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105780425"
---
# <a name="changing-registry-data"></a>Alterar dados de Registro

A classe do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para WMI tem métodos que fazem o seguinte:

-   Criar ou excluir chaves do registro.

    Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) ou [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).

-   Crie ou exclua valores nomeados, que são chamados de entradas quando estão sob chaves.

    Use o nome de um novo valor e [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)ou [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) para criar um valor nomeado. Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) para excluir um valor nomeado.

-   Altere os valores nomeados.

    Use o nome de um valor e os métodos definidos (identificados no item com marcadores anterior) para alterar os valores nomeados existentes em uma chave. Você deve saber o nome de um valor para alterá-lo. Se você não souber os nomes de valor em uma chave, use o método [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para obter os nomes.

As seções a seguir são discutidas neste tópico:

-   [Criando uma chave do registro usando o VBScript](#creating-a-registry-key-using-vbscript)
-   [Criando um valor de registro nomeado usando o PowerShell e o VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Criando uma chave do registro usando o VBScript

Como o registro é o banco de dados de configuração central para o sistema operacional, os aplicativos e os serviços, tenha cuidado ao gravar alterações em valores de registro ou excluir chaves.

> [!Note]  
> Você não pode monitorar a subchave **HKEY \_ classes \_ root** de **HKEY \_ Current \_ User (HKCU)**. O monitoramento de **HKEY \_ Users** não é recomendado porque as subchaves aparecem e desaparecem à medida que os hives são carregados.

 

Os exemplos de código a seguir mostram como criar uma nova chave do registro e uma subchave.


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Criando um valor de registro nomeado usando o PowerShell e o VBScript

O exemplo de código a seguir mostra como criar um valor nomeado chamado **multistringvalue** em **HKEY \_ local \_ Machine** \\ **software** \\ **MyKey** \\ **mysubkey** Key que o script anterior cria. O script chama [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) para gravar valores de cadeia de caracteres em um novo valor nomeado.


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

Usando o WMI, você não pode definir a segurança de acesso em uma chave do registro. No entanto, o método [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compara as configurações de segurança do usuário atual com o descritor de segurança em uma chave do registro para determinar se o usuário tem uma permissão específica, como o **\_ \_ valor do conjunto de chaves**.
