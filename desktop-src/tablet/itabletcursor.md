---
description: Representa um objeto de caneta.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interface ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837221"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="82236-103">Interface ITabletCursor</span><span class="sxs-lookup"><span data-stu-id="82236-103">ITabletCursor interface</span></span>

<span data-ttu-id="82236-104">Representa um objeto de caneta.</span><span class="sxs-lookup"><span data-stu-id="82236-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="82236-105">Membros</span><span class="sxs-lookup"><span data-stu-id="82236-105">Members</span></span>

<span data-ttu-id="82236-106">A interface **ITabletCursor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="82236-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="82236-107">**ITabletCursor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="82236-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="82236-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="82236-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82236-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="82236-109">Methods</span></span>

<span data-ttu-id="82236-110">A interface **ITabletCursor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="82236-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="82236-111">Método</span><span class="sxs-lookup"><span data-stu-id="82236-111">Method</span></span>                                                 | <span data-ttu-id="82236-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="82236-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="82236-113">**Getbutton**</span><span class="sxs-lookup"><span data-stu-id="82236-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="82236-114">Recupera o objeto de botão especificado de uma caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="82236-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="82236-115">**GetButtonCount**</span><span class="sxs-lookup"><span data-stu-id="82236-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="82236-116">Recupera o número de botões na caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="82236-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="82236-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="82236-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="82236-118">Recupera o identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="82236-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="82236-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="82236-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="82236-120">Recupera o nome da caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="82236-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="82236-121">**Isverted**</span><span class="sxs-lookup"><span data-stu-id="82236-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="82236-122">Indica se a caneta está de cabeça para baixo.</span><span class="sxs-lookup"><span data-stu-id="82236-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="82236-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="82236-123">Remarks</span></span>

<span data-ttu-id="82236-124">Não use essa interface.</span><span class="sxs-lookup"><span data-stu-id="82236-124">Do not use this interface.</span></span>

<span data-ttu-id="82236-125">O código a seguir descreve como a interface **ITabletCursor** é definida.</span><span class="sxs-lookup"><span data-stu-id="82236-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="82236-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82236-126">Requirements</span></span>



| <span data-ttu-id="82236-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="82236-127">Requirement</span></span> | <span data-ttu-id="82236-128">Valor</span><span class="sxs-lookup"><span data-stu-id="82236-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82236-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82236-129">Minimum supported client</span></span><br/> | <span data-ttu-id="82236-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="82236-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="82236-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82236-131">Minimum supported server</span></span><br/> | <span data-ttu-id="82236-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="82236-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="82236-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82236-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="82236-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82236-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

