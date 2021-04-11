---
description: Representa informações gerais sobre um botão em um dispositivo de caneta.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interface ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297022"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="77369-103">Interface ITabletCursorButton</span><span class="sxs-lookup"><span data-stu-id="77369-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="77369-104">Representa informações gerais sobre um botão em um dispositivo de caneta.</span><span class="sxs-lookup"><span data-stu-id="77369-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="77369-105">Membros</span><span class="sxs-lookup"><span data-stu-id="77369-105">Members</span></span>

<span data-ttu-id="77369-106">A interface **ITabletCursorButton** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="77369-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77369-107">**ITabletCursorButton** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77369-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="77369-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="77369-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77369-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="77369-109">Methods</span></span>

<span data-ttu-id="77369-110">A interface **ITabletCursorButton** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="77369-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="77369-111">Método</span><span class="sxs-lookup"><span data-stu-id="77369-111">Method</span></span>                                         | <span data-ttu-id="77369-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="77369-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="77369-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="77369-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="77369-114">Recupera o identificador exclusivo do botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="77369-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="77369-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="77369-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="77369-116">Recupera o nome do botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="77369-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="77369-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="77369-117">Remarks</span></span>

<span data-ttu-id="77369-118">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="77369-118">Developers should not use this interface.</span></span>

<span data-ttu-id="77369-119">O código a seguir mostra como a interface **ITabletCursorButton** é definida.</span><span class="sxs-lookup"><span data-stu-id="77369-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="77369-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77369-120">Requirements</span></span>



| <span data-ttu-id="77369-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="77369-121">Requirement</span></span> | <span data-ttu-id="77369-122">Valor</span><span class="sxs-lookup"><span data-stu-id="77369-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77369-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77369-123">Minimum supported client</span></span><br/> | <span data-ttu-id="77369-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="77369-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="77369-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77369-125">Minimum supported server</span></span><br/> | <span data-ttu-id="77369-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77369-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="77369-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77369-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="77369-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77369-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77369-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="77369-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77369-130">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="77369-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

