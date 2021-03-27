---
description: Contém informações que o Gerenciador de arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de arquivos. A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de arquivos tiver carregado o menu.
title: Estrutura de FMS_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967284"
---
# <a name="fms_load-structure"></a><span data-ttu-id="ab266-104">Estrutura de carregamento do FMS \_</span><span class="sxs-lookup"><span data-stu-id="ab266-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="ab266-105">Contém informações que o Gerenciador de arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab266-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="ab266-106">A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de arquivos tiver carregado o menu.</span><span class="sxs-lookup"><span data-stu-id="ab266-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab266-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab266-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="ab266-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ab266-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab266-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="ab266-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="ab266-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ab266-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ab266-111">O comprimento, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ab266-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ab266-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="ab266-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="ab266-113">Tipo: **o \[ texto do menu TCHAR é \_ \_ Len \]**</span><span class="sxs-lookup"><span data-stu-id="ab266-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="ab266-114">Um nome finalizado por nulo para um item de menu que aparece na barra de menus no Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab266-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="ab266-115">**hMenu**</span><span class="sxs-lookup"><span data-stu-id="ab266-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="ab266-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="ab266-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="ab266-117">O identificador do menu pop-up adicionado à barra de menus no Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab266-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="ab266-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="ab266-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="ab266-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="ab266-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="ab266-120">O valor delta do item de menu.</span><span class="sxs-lookup"><span data-stu-id="ab266-120">The menu item delta value.</span></span> <span data-ttu-id="ab266-121">Para evitar conflitos com seus próprios itens de menu, o Gerenciador de arquivos renumera os identificadores de item de menu no menu pop-up identificado pelo membro **HMENU** adicionando esse valor delta a cada identificador.</span><span class="sxs-lookup"><span data-stu-id="ab266-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="ab266-122">Uma DLL de extensão que deve modificar um item de menu deve identificar o item adicionando o valor delta ao identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="ab266-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="ab266-123">O valor desse membro pode variar de uma sessão para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="ab266-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab266-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab266-124">Requirements</span></span>



| <span data-ttu-id="ab266-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab266-125">Requirement</span></span> | <span data-ttu-id="ab266-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ab266-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab266-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab266-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ab266-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab266-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ab266-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab266-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ab266-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab266-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ab266-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab266-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab266-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab266-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab266-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab266-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab266-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="ab266-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




