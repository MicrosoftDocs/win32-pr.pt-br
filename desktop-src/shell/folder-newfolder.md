---
description: Cria uma nova pasta.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Método Folder. NewFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921680"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="a0052-103">Método Folder. NewFolder</span><span class="sxs-lookup"><span data-stu-id="a0052-103">Folder.NewFolder method</span></span>

<span data-ttu-id="a0052-104">Cria uma nova pasta.</span><span class="sxs-lookup"><span data-stu-id="a0052-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0052-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0052-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="a0052-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0052-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0052-107">*bName*</span><span class="sxs-lookup"><span data-stu-id="a0052-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="a0052-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a0052-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a0052-109">Uma cadeia de caracteres que especifica o nome da nova pasta.</span><span class="sxs-lookup"><span data-stu-id="a0052-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="a0052-110">*vOptions* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="a0052-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0052-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="a0052-111">Type: **Variant**</span></span>

<span data-ttu-id="a0052-112">Esse valor não é usado atualmente.</span><span class="sxs-lookup"><span data-stu-id="a0052-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0052-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0052-113">Return value</span></span>

<span data-ttu-id="a0052-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a0052-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0052-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0052-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a0052-116">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="a0052-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="a0052-117">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="a0052-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="a0052-118">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="a0052-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a0052-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0052-119">Examples</span></span>

<span data-ttu-id="a0052-120">O exemplo a seguir usa **NewFolder** para criar a nova pasta C: \\ TestFolder.</span><span class="sxs-lookup"><span data-stu-id="a0052-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="a0052-121">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a0052-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a0052-122">JScript</span><span class="sxs-lookup"><span data-stu-id="a0052-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="a0052-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="a0052-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="a0052-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a0052-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a0052-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0052-125">Requirements</span></span>



| <span data-ttu-id="a0052-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0052-126">Requirement</span></span> | <span data-ttu-id="a0052-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a0052-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0052-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0052-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0052-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0052-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0052-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0052-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0052-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0052-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0052-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0052-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0052-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0052-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a0052-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="a0052-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0052-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0052-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a0052-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0052-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0052-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a0052-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
