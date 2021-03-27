---
description: Recupera um objeto InternetExplorer que representa a janela do Shell.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Método ShellWindows. Item (textdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169905"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="e437d-103">Método ShellWindows. Item</span><span class="sxs-lookup"><span data-stu-id="e437d-103">ShellWindows.Item method</span></span>

<span data-ttu-id="e437d-104">Recupera um objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="e437d-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e437d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e437d-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="e437d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e437d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e437d-107">*iIndex* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e437d-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e437d-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="e437d-108">Type: **Variant**</span></span>

<span data-ttu-id="e437d-109">O índice com base em zero do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e437d-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="e437d-110">Esse valor deve ser menor que o valor da propriedade [**Count**](shellwindows-count.md) .</span><span class="sxs-lookup"><span data-stu-id="e437d-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="e437d-111">Se esse valor for omitido, será usado um valor padrão de 0.</span><span class="sxs-lookup"><span data-stu-id="e437d-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e437d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e437d-112">Return value</span></span>

<span data-ttu-id="e437d-113">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="e437d-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="e437d-114">Uma referência de objeto para o objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="e437d-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="e437d-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e437d-115">Examples</span></span>

<span data-ttu-id="e437d-116">O exemplo a seguir usa [**Item**](folderitemverbs-item.md) para recuperar o objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa o primeiro item de janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="e437d-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="e437d-117">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e437d-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e437d-118">JScript</span><span class="sxs-lookup"><span data-stu-id="e437d-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="e437d-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="e437d-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e437d-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e437d-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e437d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e437d-121">Requirements</span></span>



| <span data-ttu-id="e437d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e437d-122">Requirement</span></span> | <span data-ttu-id="e437d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e437d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e437d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e437d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e437d-125">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e437d-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e437d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e437d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e437d-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e437d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e437d-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e437d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e437d-129"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e437d-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e437d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e437d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e437d-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e437d-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
