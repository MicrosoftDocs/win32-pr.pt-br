---
description: Obtém o valor de uma política especificada do Windows Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Método IShellDispatch4. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827397"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="50a90-103">Método IShellDispatch4. ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="50a90-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="50a90-104">Obtém o valor de uma política especificada do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="50a90-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="50a90-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50a90-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="50a90-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50a90-107">*bstrPolicyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50a90-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50a90-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="50a90-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="50a90-109">Uma **cadeia de caracteres** que especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="50a90-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50a90-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50a90-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="50a90-111">JScript</span><span class="sxs-lookup"><span data-stu-id="50a90-111">JScript</span></span>

<span data-ttu-id="50a90-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="50a90-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="50a90-113">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="50a90-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="50a90-114">VB</span><span class="sxs-lookup"><span data-stu-id="50a90-114">VB</span></span>

<span data-ttu-id="50a90-115">Tipo: _*variante \**_</span><span class="sxs-lookup"><span data-stu-id="50a90-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="50a90-116">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="50a90-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="50a90-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="50a90-117">Remarks</span></span>

<span data-ttu-id="50a90-118">Os administradores de rede podem controlar e gerenciar o ambiente computacional de seus usuários definindo políticas.</span><span class="sxs-lookup"><span data-stu-id="50a90-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="50a90-119">O nome do valor especificado deve estar na subchave _ \*HKEY \_ \_ **\\** software do usuário atual **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*.</span><span class="sxs-lookup"><span data-stu-id="50a90-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="50a90-120">Se o nome do valor não existir, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50a90-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="50a90-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50a90-121">Examples</span></span>

<span data-ttu-id="50a90-122">Os exemplos a seguir mostram o uso apropriado de **ExplorerPolicy** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="50a90-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="50a90-123">JScript</span><span class="sxs-lookup"><span data-stu-id="50a90-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="50a90-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="50a90-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="50a90-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="50a90-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="50a90-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50a90-126">Requirements</span></span>



| <span data-ttu-id="50a90-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="50a90-127">Requirement</span></span> | <span data-ttu-id="50a90-128">Valor</span><span class="sxs-lookup"><span data-stu-id="50a90-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a90-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50a90-129">Minimum supported client</span></span><br/> | <span data-ttu-id="50a90-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="50a90-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="50a90-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50a90-131">Minimum supported server</span></span><br/> | <span data-ttu-id="50a90-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50a90-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="50a90-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50a90-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="50a90-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50a90-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="50a90-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="50a90-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50a90-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50a90-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="50a90-137">DLL</span><span class="sxs-lookup"><span data-stu-id="50a90-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50a90-138"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="50a90-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
