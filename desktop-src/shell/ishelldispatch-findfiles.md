---
description: 'Exibe a caixa de diálogo localizar: todos os arquivos. Isso é o mesmo que clicar no menu iniciar e Selecionar Pesquisar.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Método IShellDispatch. FindFiles (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827403"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="b4ef5-104">Método IShellDispatch. FindFiles</span><span class="sxs-lookup"><span data-stu-id="b4ef5-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="b4ef5-105">Exibe a caixa de diálogo **localizar: todos os arquivos** .</span><span class="sxs-lookup"><span data-stu-id="b4ef5-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="b4ef5-106">Isso é o mesmo que clicar no menu **Iniciar** e selecionar **Pesquisar**.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ef5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4ef5-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="b4ef5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4ef5-108">Parameters</span></span>

<span data-ttu-id="b4ef5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4ef5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4ef5-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b4ef5-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b4ef5-111">JScript</span></span>

<span data-ttu-id="b4ef5-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b4ef5-113">VB</span><span class="sxs-lookup"><span data-stu-id="b4ef5-113">VB</span></span>

<span data-ttu-id="b4ef5-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ef5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4ef5-115">Remarks</span></span>

<span data-ttu-id="b4ef5-116">Esse método é implementado e acessado por meio do método [**shell. findfiles**](shell-findfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ef5-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b4ef5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4ef5-117">Examples</span></span>

<span data-ttu-id="b4ef5-118">Os exemplos a seguir mostram o uso de **FindFiles** em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b4ef5-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b4ef5-119">JScript</span><span class="sxs-lookup"><span data-stu-id="b4ef5-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="b4ef5-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="b4ef5-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="b4ef5-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b4ef5-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b4ef5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4ef5-122">Requirements</span></span>



| <span data-ttu-id="b4ef5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4ef5-123">Requirement</span></span> | <span data-ttu-id="b4ef5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b4ef5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ef5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4ef5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ef5-126">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4ef5-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4ef5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4ef5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ef5-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b4ef5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4ef5-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b4ef5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4ef5-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ef5-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b4ef5-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="b4ef5-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4ef5-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4ef5-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b4ef5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b4ef5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4ef5-134"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b4ef5-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




