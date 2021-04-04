---
title: Método WebViewFolderContents. PopupItemMenu (shldisp. h)
description: Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Recursos do ambiente Windows herdado do método PopupItemMenu
- Método PopupItemMenu recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644306"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="7c2eb-106">Método WebViewFolderContents. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="7c2eb-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="7c2eb-107">Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c2eb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c2eb-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="7c2eb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c2eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c2eb-110">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7c2eb-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2eb-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="7c2eb-111">Type: **Variant**</span></span>

<span data-ttu-id="7c2eb-112">O objeto [**FolderItem**](../shell/folderitem.md) para o qual o menu de atalho será criado.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="7c2eb-113">*VX* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c2eb-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2eb-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="7c2eb-114">Type: **Variant**</span></span>

<span data-ttu-id="7c2eb-115">A posição horizontal do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7c2eb-116">*Vy* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7c2eb-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7c2eb-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="7c2eb-117">Type: **Variant**</span></span>

<span data-ttu-id="7c2eb-118">A posição vertical do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c2eb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c2eb-119">Return value</span></span>

<span data-ttu-id="7c2eb-120">Tipo: \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="7c2eb-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="7c2eb-121">Quando esse método retorna, contém a cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="7c2eb-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c2eb-122">Examples</span></span>

<span data-ttu-id="7c2eb-123">O exemplo a seguir mostra o uso apropriado de _ *PopupItemMenu*\* para JScript Embedded em HTML.</span><span class="sxs-lookup"><span data-stu-id="7c2eb-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="7c2eb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c2eb-124">Requirements</span></span>



| <span data-ttu-id="7c2eb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c2eb-125">Requirement</span></span> | <span data-ttu-id="7c2eb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7c2eb-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2eb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c2eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7c2eb-128">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7c2eb-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c2eb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c2eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7c2eb-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c2eb-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c2eb-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c2eb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c2eb-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c2eb-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7c2eb-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="7c2eb-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c2eb-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c2eb-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7c2eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7c2eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c2eb-136"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7c2eb-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

