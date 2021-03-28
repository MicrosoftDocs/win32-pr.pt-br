---
description: Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
title: Método ShellFolderView. PopupItemMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171180"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="307b3-103">Método ShellFolderView. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="307b3-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="307b3-104">Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.</span><span class="sxs-lookup"><span data-stu-id="307b3-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="307b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="307b3-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="307b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="307b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="307b3-107">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="307b3-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="307b3-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="307b3-108">Type: **Variant**</span></span>

<span data-ttu-id="307b3-109">O objeto [**FolderItem**](folderitem.md) para o qual o menu de atalho será criado.</span><span class="sxs-lookup"><span data-stu-id="307b3-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="307b3-110">*VX* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="307b3-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="307b3-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="307b3-111">Type: **Variant**</span></span>

<span data-ttu-id="307b3-112">A posição horizontal do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="307b3-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="307b3-113">*Vy* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="307b3-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="307b3-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="307b3-114">Type: **Variant**</span></span>

<span data-ttu-id="307b3-115">A posição vertical do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="307b3-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="307b3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="307b3-116">Return value</span></span>

<span data-ttu-id="307b3-117">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="307b3-117">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="307b3-118">A *cadeia de caracteres* _ \* que recebe a cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="307b3-118">The _ *String*\* that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="307b3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="307b3-119">Requirements</span></span>



| <span data-ttu-id="307b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="307b3-120">Requirement</span></span> | <span data-ttu-id="307b3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="307b3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307b3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="307b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="307b3-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="307b3-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="307b3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="307b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="307b3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="307b3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="307b3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="307b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="307b3-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="307b3-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="307b3-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="307b3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="307b3-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="307b3-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="307b3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="307b3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="307b3-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="307b3-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
