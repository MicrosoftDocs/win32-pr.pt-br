---
description: Obtém um objeto que representa o pai do objeto atual.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Propriedade Shell. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967955"
---
# <a name="shellparent-property"></a><span data-ttu-id="35110-103">Propriedade Shell. Parent</span><span class="sxs-lookup"><span data-stu-id="35110-103">Shell.Parent property</span></span>

<span data-ttu-id="35110-104">Obtém um objeto que representa o pai do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="35110-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="35110-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="35110-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35110-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35110-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="35110-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35110-107">Property value</span></span>

<span data-ttu-id="35110-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto pai.</span><span class="sxs-lookup"><span data-stu-id="35110-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="35110-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35110-109">Examples</span></span>

<span data-ttu-id="35110-110">O exemplo a seguir mostra o uso apropriado do **pai** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="35110-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="35110-111">JScript</span><span class="sxs-lookup"><span data-stu-id="35110-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="35110-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="35110-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="35110-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="35110-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="35110-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35110-114">Requirements</span></span>



| <span data-ttu-id="35110-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35110-115">Requirement</span></span> | <span data-ttu-id="35110-116">Valor</span><span class="sxs-lookup"><span data-stu-id="35110-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35110-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35110-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35110-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35110-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35110-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35110-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35110-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35110-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35110-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="35110-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35110-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35110-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="35110-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="35110-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35110-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35110-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="35110-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35110-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35110-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="35110-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
