---
description: Método ShellFolderView. PopupItemMenu – cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840747"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="9a257-103">Método ShellFolderView. PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="9a257-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="9a257-104">Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.</span><span class="sxs-lookup"><span data-stu-id="9a257-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a257-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a257-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="9a257-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a257-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a257-107">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a257-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a257-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9a257-108">Type: **Variant**</span></span>

<span data-ttu-id="9a257-109">O objeto [**FolderItem**](folderitem.md) para o qual o menu de atalho será criado.</span><span class="sxs-lookup"><span data-stu-id="9a257-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="9a257-110">*VX* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9a257-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a257-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9a257-111">Type: **Variant**</span></span>

<span data-ttu-id="9a257-112">A posição horizontal do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="9a257-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9a257-113">*Vy* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9a257-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a257-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="9a257-114">Type: **Variant**</span></span>

<span data-ttu-id="9a257-115">A posição vertical do menu, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="9a257-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a257-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a257-116">Return value</span></span>

<span data-ttu-id="9a257-117">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="9a257-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="9a257-118">A **cadeia de caracteres** que recebe a cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="9a257-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a257-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a257-119">Requirements</span></span>



| <span data-ttu-id="9a257-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a257-120">Requirement</span></span> | <span data-ttu-id="9a257-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9a257-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a257-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a257-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a257-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9a257-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a257-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a257-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a257-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a257-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a257-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a257-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a257-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a257-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9a257-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="9a257-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a257-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a257-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9a257-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9a257-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a257-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9a257-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
