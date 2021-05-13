---
description: Contém informações que o Gerenciador de Arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de Arquivos. A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de Arquivos carregar o menu.
title: FMS_LOAD estrutura (Wfext.h)
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
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842187"
---
# <a name="fms_load-structure"></a><span data-ttu-id="40425-104">Estrutura FMS \_ LOAD</span><span class="sxs-lookup"><span data-stu-id="40425-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="40425-105">Contém informações que o Gerenciador de Arquivos usa para adicionar um menu personalizado fornecido por uma DLL de extensão do Gerenciador de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="40425-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="40425-106">A estrutura também fornece um valor delta que a DLL de extensão pode usar para manipular o menu personalizado depois que o Gerenciador de Arquivos carregar o menu.</span><span class="sxs-lookup"><span data-stu-id="40425-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="40425-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40425-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="40425-108">Membros</span><span class="sxs-lookup"><span data-stu-id="40425-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="40425-109">**Dwsize**</span><span class="sxs-lookup"><span data-stu-id="40425-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="40425-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="40425-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="40425-111">O comprimento, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="40425-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="40425-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="40425-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="40425-113">Tipo: **LEN DE TEXTO DO \[ MENU \_ \_ \] TCHAR**</span><span class="sxs-lookup"><span data-stu-id="40425-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="40425-114">Um nome terminado em nulo para um item de menu que aparece na barra de menus no Gerenciador de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="40425-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="40425-115">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="40425-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="40425-116">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="40425-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="40425-117">O identificador do menu pop-up adicionado à barra de menus no Gerenciador de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="40425-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="40425-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="40425-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="40425-119">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="40425-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="40425-120">O valor delta do item de menu.</span><span class="sxs-lookup"><span data-stu-id="40425-120">The menu item delta value.</span></span> <span data-ttu-id="40425-121">Para evitar conflitos com seus próprios itens de menu, o Gerenciador de Arquivos renumera os identificadores de item de menu no menu pop-up identificado pelo membro **hMenu** adicionando esse valor delta a cada identificador.</span><span class="sxs-lookup"><span data-stu-id="40425-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="40425-122">Uma DLL de extensão que deve modificar um item de menu deve identificar o item adicionando o valor delta ao identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="40425-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="40425-123">O valor desse membro pode variar de uma sessão para uma sessão.</span><span class="sxs-lookup"><span data-stu-id="40425-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40425-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40425-124">Requirements</span></span>



| <span data-ttu-id="40425-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="40425-125">Requirement</span></span> | <span data-ttu-id="40425-126">Valor</span><span class="sxs-lookup"><span data-stu-id="40425-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40425-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40425-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40425-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40425-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="40425-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40425-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40425-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40425-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="40425-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40425-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40425-132"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="40425-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40425-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="40425-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40425-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="40425-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




