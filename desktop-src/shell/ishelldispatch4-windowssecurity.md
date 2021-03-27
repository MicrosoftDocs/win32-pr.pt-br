---
description: Exibe a caixa de diálogo Segurança do Windows.
title: Método IShellDispatch4. WindowsSecurity (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 066321c0ea4e4d5ade35a6571c59128a5137cba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967506"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="009ef-103">Método IShellDispatch4. WindowsSecurity</span><span class="sxs-lookup"><span data-stu-id="009ef-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="009ef-104">Exibe a caixa de diálogo **segurança do Windows** .</span><span class="sxs-lookup"><span data-stu-id="009ef-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="009ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="009ef-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="009ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="009ef-106">Parameters</span></span>

<span data-ttu-id="009ef-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="009ef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="009ef-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="009ef-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="009ef-109">JScript</span><span class="sxs-lookup"><span data-stu-id="009ef-109">JScript</span></span>

<span data-ttu-id="009ef-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="009ef-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="009ef-111">VB</span><span class="sxs-lookup"><span data-stu-id="009ef-111">VB</span></span>

<span data-ttu-id="009ef-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="009ef-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="009ef-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="009ef-113">Remarks</span></span>

<span data-ttu-id="009ef-114">Esse método exibe a caixa de diálogo mostrada após pressionar CTRL + ALT + DELETE ou usar a opção de segurança no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="009ef-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="009ef-115">Esse método pode ser usado somente quando conectado por uma sessão de terminal ao Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="009ef-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="009ef-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="009ef-116">Examples</span></span>

<span data-ttu-id="009ef-117">Os exemplos a seguir mostram o uso de **WindowsSecurity** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="009ef-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="009ef-118">JScript</span><span class="sxs-lookup"><span data-stu-id="009ef-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="009ef-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="009ef-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="009ef-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="009ef-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="009ef-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="009ef-121">Requirements</span></span>



| <span data-ttu-id="009ef-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="009ef-122">Requirement</span></span> | <span data-ttu-id="009ef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="009ef-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="009ef-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="009ef-124">Minimum supported client</span></span><br/> | <span data-ttu-id="009ef-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="009ef-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="009ef-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="009ef-126">Minimum supported server</span></span><br/> | <span data-ttu-id="009ef-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="009ef-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="009ef-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="009ef-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="009ef-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="009ef-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="009ef-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="009ef-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="009ef-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="009ef-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="009ef-132">DLL</span><span class="sxs-lookup"><span data-stu-id="009ef-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="009ef-133"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="009ef-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




