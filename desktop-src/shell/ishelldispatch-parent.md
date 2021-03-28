---
description: Recupera um objeto que representa o pai do objeto atual.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Propriedade IShellDispatch. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090843"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="2aa89-103">Propriedade IShellDispatch. Parent</span><span class="sxs-lookup"><span data-stu-id="2aa89-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="2aa89-104">Recupera um objeto que representa o pai do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="2aa89-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="2aa89-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2aa89-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa89-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aa89-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="2aa89-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2aa89-107">Property value</span></span>

<span data-ttu-id="2aa89-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto pai.</span><span class="sxs-lookup"><span data-stu-id="2aa89-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa89-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2aa89-109">Remarks</span></span>

<span data-ttu-id="2aa89-110">Essa propriedade é implementada e acessada por meio da propriedade [**shell. Parent**](shell-parent.md) .</span><span class="sxs-lookup"><span data-stu-id="2aa89-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2aa89-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2aa89-111">Examples</span></span>

<span data-ttu-id="2aa89-112">Os exemplos a seguir mostram o uso de **pai** no JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2aa89-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2aa89-113">JScript</span><span class="sxs-lookup"><span data-stu-id="2aa89-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="2aa89-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="2aa89-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2aa89-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2aa89-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2aa89-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aa89-116">Requirements</span></span>



| <span data-ttu-id="2aa89-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aa89-117">Requirement</span></span> | <span data-ttu-id="2aa89-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2aa89-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa89-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aa89-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2aa89-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2aa89-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2aa89-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aa89-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2aa89-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2aa89-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2aa89-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2aa89-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aa89-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa89-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2aa89-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="2aa89-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2aa89-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2aa89-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2aa89-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2aa89-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aa89-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2aa89-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
