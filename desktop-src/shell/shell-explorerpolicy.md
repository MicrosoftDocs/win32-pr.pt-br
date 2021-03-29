---
description: Obtém o valor de uma política especificada do Windows Internet Explorer.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Método Shell. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968228"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="85373-103">Método Shell. ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="85373-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="85373-104">Obtém o valor de uma política especificada do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="85373-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="85373-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85373-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="85373-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85373-107">*bstrPolicyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85373-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85373-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="85373-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="85373-109">Uma **cadeia de caracteres** que especifica o nome da política.</span><span class="sxs-lookup"><span data-stu-id="85373-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85373-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85373-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="85373-111">JScript</span><span class="sxs-lookup"><span data-stu-id="85373-111">JScript</span></span>

<span data-ttu-id="85373-112">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="85373-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="85373-113">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="85373-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="85373-114">VB</span><span class="sxs-lookup"><span data-stu-id="85373-114">VB</span></span>

<span data-ttu-id="85373-115">Tipo: _*variante \**_</span><span class="sxs-lookup"><span data-stu-id="85373-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="85373-116">O valor associado ao nome de política especificado.</span><span class="sxs-lookup"><span data-stu-id="85373-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="85373-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="85373-117">Remarks</span></span>

<span data-ttu-id="85373-118">Os administradores de rede podem controlar e gerenciar o ambiente computacional de seus usuários definindo políticas.</span><span class="sxs-lookup"><span data-stu-id="85373-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="85373-119">O nome do valor especificado deve estar na subchave _ \*HKEY \_ \_ **\\** software do usuário atual **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*.</span><span class="sxs-lookup"><span data-stu-id="85373-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="85373-120">Se o nome do valor não existir, o método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="85373-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="85373-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85373-121">Examples</span></span>

<span data-ttu-id="85373-122">Os exemplos a seguir mostram o uso apropriado de **ExplorerPolicy** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="85373-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="85373-123">JScript</span><span class="sxs-lookup"><span data-stu-id="85373-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="85373-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="85373-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="85373-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="85373-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="85373-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85373-126">Requirements</span></span>



| <span data-ttu-id="85373-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="85373-127">Requirement</span></span> | <span data-ttu-id="85373-128">Valor</span><span class="sxs-lookup"><span data-stu-id="85373-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85373-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85373-129">Minimum supported client</span></span><br/> | <span data-ttu-id="85373-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="85373-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="85373-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85373-131">Minimum supported server</span></span><br/> | <span data-ttu-id="85373-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85373-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="85373-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85373-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="85373-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85373-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="85373-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="85373-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85373-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85373-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="85373-137">DLL</span><span class="sxs-lookup"><span data-stu-id="85373-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85373-138"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="85373-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
