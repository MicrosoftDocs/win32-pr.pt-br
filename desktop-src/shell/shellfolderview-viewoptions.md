---
description: Obtém um conjunto de sinalizadores que indicam as opções atuais da exibição.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Propriedade ShellFolderView. ViewOptions (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989061"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="46650-103">Propriedade ShellFolderView. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="46650-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="46650-104">Obtém um conjunto de sinalizadores que indicam as opções atuais da exibição.</span><span class="sxs-lookup"><span data-stu-id="46650-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="46650-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="46650-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46650-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46650-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="46650-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="46650-107">Property value</span></span>

<span data-ttu-id="46650-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de opções de exibição.</span><span class="sxs-lookup"><span data-stu-id="46650-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="46650-109">Contém um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="46650-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="46650-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="46650-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="46650-111">A opção **Mostrar todos os arquivos** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="46650-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ Conextensões** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="46650-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="46650-113">A opção **Ocultar extensões para tipos de arquivo conhecidos** está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="46650-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="46650-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="46650-115">A opção **Exibir arquivos compactados e pastas com cores alternativas** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="46650-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="46650-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="46650-117">A opção **não mostrar arquivos ocultos** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="46650-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="46650-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="46650-119">A opção **estilo clássico** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="46650-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="46650-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="46650-121">A opção **clique duas vezes para abrir um item** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="46650-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="46650-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="46650-123">A opção **Active Desktop – exibir como página da Web** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="46650-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46650-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="46650-124">Remarks</span></span>

<span data-ttu-id="46650-125">[**FocusedItem**](shellfolderview-focuseditem.md) só pode ser chamado no sistema local.</span><span class="sxs-lookup"><span data-stu-id="46650-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="46650-126">Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.</span><span class="sxs-lookup"><span data-stu-id="46650-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="46650-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46650-127">Examples</span></span>

<span data-ttu-id="46650-128">O exemplo a seguir mostra o uso apropriado desse método no JScript inserido em HTML.</span><span class="sxs-lookup"><span data-stu-id="46650-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="46650-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46650-129">Requirements</span></span>



| <span data-ttu-id="46650-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="46650-130">Requirement</span></span> | <span data-ttu-id="46650-131">Valor</span><span class="sxs-lookup"><span data-stu-id="46650-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46650-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46650-132">Minimum supported client</span></span><br/> | <span data-ttu-id="46650-133">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="46650-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46650-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46650-134">Minimum supported server</span></span><br/> | <span data-ttu-id="46650-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46650-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46650-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46650-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="46650-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46650-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="46650-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="46650-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46650-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46650-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="46650-140">DLL</span><span class="sxs-lookup"><span data-stu-id="46650-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46650-141"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="46650-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
