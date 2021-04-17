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
# <a name="changing-registry-data"></a><span data-ttu-id="36aa6-103">Alterar dados de Registro</span><span class="sxs-lookup"><span data-stu-id="36aa6-103">Changing Registry Data</span></span>

<span data-ttu-id="36aa6-104">A classe do [provedor de registro do sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para WMI tem métodos que fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="36aa6-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="36aa6-105">Criar ou excluir chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="36aa6-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="36aa6-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) ou [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="36aa6-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="36aa6-107">Crie ou exclua valores nomeados, que são chamados de entradas quando estão sob chaves.</span><span class="sxs-lookup"><span data-stu-id="36aa6-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="36aa6-108">Use o nome de um novo valor e [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)ou [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) para criar um valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="36aa6-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="36aa6-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) para excluir um valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="36aa6-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="36aa6-110">Altere os valores nomeados.</span><span class="sxs-lookup"><span data-stu-id="36aa6-110">Change named values.</span></span>

    <span data-ttu-id="36aa6-111">Use o nome de um valor e os métodos definidos (identificados no item com marcadores anterior) para alterar os valores nomeados existentes em uma chave.</span><span class="sxs-lookup"><span data-stu-id="36aa6-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="36aa6-112">Você deve saber o nome de um valor para alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="36aa6-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="36aa6-113">Se você não souber os nomes de valor em uma chave, use o método [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para obter os nomes.</span><span class="sxs-lookup"><span data-stu-id="36aa6-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="36aa6-114">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="36aa6-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="36aa6-115">Criando uma chave do registro usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="36aa6-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="36aa6-116">Criando um valor de registro nomeado usando o PowerShell e o VBScript</span><span class="sxs-lookup"><span data-stu-id="36aa6-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="36aa6-117">Criando uma chave do registro usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="36aa6-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="36aa6-118">Como o registro é o banco de dados de configuração central para o sistema operacional, os aplicativos e os serviços, tenha cuidado ao gravar alterações em valores de registro ou excluir chaves.</span><span class="sxs-lookup"><span data-stu-id="36aa6-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="36aa6-119">Você não pode monitorar a subchave **HKEY \_ classes \_ root** de **HKEY \_ Current \_ User (HKCU)**.</span><span class="sxs-lookup"><span data-stu-id="36aa6-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="36aa6-120">O monitoramento de **HKEY \_ Users** não é recomendado porque as subchaves aparecem e desaparecem à medida que os hives são carregados.</span><span class="sxs-lookup"><span data-stu-id="36aa6-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="36aa6-121">Os exemplos de código a seguir mostram como criar uma nova chave do registro e uma subchave.</span><span class="sxs-lookup"><span data-stu-id="36aa6-121">The following code examples show how to create a new registry key and a subkey.</span></span>


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="36aa6-122">Criando um valor de registro nomeado usando o PowerShell e o VBScript</span><span class="sxs-lookup"><span data-stu-id="36aa6-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="36aa6-123">O exemplo de código a seguir mostra como criar um valor nomeado chamado **multistringvalue** em **HKEY \_ local \_ Machine** \\ **software** \\ **MyKey** \\ **mysubkey** Key que o script anterior cria.</span><span class="sxs-lookup"><span data-stu-id="36aa6-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="36aa6-124">O script chama [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) para gravar valores de cadeia de caracteres em um novo valor nomeado.</span><span class="sxs-lookup"><span data-stu-id="36aa6-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


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

<span data-ttu-id="36aa6-125">Usando o WMI, você não pode definir a segurança de acesso em uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="36aa6-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="36aa6-126">No entanto, o método [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compara as configurações de segurança do usuário atual com o descritor de segurança em uma chave do registro para determinar se o usuário tem uma permissão específica, como o **\_ \_ valor do conjunto de chaves**.</span><span class="sxs-lookup"><span data-stu-id="36aa6-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
