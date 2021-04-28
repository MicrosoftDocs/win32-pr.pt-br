---
description: Método IShellDispatch4. ExplorerPolicy – Obtém o valor de uma política especificada do Windows Internet Explorer.
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
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116824"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="6ea4c-103">Método IShellDispatch4. ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="6ea4c-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="6ea4c-104">Obtém o valor de uma política especificada do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea4c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ea4c-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="6ea4c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ea4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea4c-107">*bstrPolicyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ea4c-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea4c-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6ea4c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6ea4c-109">Uma **cadeia de caracteres** que especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea4c-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6ea4c-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6ea4c-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6ea4c-111">JScript</span></span>

<span data-ttu-id="6ea4c-112">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6ea4c-112">Type: **Variant\***</span></span>

<span data-ttu-id="6ea4c-113">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="6ea4c-114">VB</span><span class="sxs-lookup"><span data-stu-id="6ea4c-114">VB</span></span>

<span data-ttu-id="6ea4c-115">Tipo: **variante \***</span><span class="sxs-lookup"><span data-stu-id="6ea4c-115">Type: **Variant\***</span></span>

<span data-ttu-id="6ea4c-116">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea4c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ea4c-117">Remarks</span></span>

<span data-ttu-id="6ea4c-118">Os administradores de rede podem controlar e gerenciar o ambiente computacional de seus usuários definindo políticas.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="6ea4c-119">O nome do valor especificado deve estar dentro da subchave do **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer** .</span><span class="sxs-lookup"><span data-stu-id="6ea4c-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="6ea4c-120">Se o nome do valor não existir, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="6ea4c-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ea4c-121">Examples</span></span>

<span data-ttu-id="6ea4c-122">Os exemplos a seguir mostram o uso apropriado de **ExplorerPolicy** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6ea4c-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6ea4c-123">JScript</span><span class="sxs-lookup"><span data-stu-id="6ea4c-123">JScript:</span></span>


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



<span data-ttu-id="6ea4c-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="6ea4c-124">VBScript:</span></span>


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



<span data-ttu-id="6ea4c-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6ea4c-125">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6ea4c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ea4c-126">Requirements</span></span>



| <span data-ttu-id="6ea4c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ea4c-127">Requirement</span></span> | <span data-ttu-id="6ea4c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6ea4c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea4c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ea4c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea4c-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ea4c-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="6ea4c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ea4c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea4c-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ea4c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ea4c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ea4c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ea4c-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea4c-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6ea4c-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="6ea4c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ea4c-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ea4c-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6ea4c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea4c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea4c-138"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6ea4c-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
