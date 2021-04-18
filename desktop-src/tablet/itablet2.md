---
description: Estende a interface ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interface ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780717"
---
# <a name="itablet2-interface"></a><span data-ttu-id="dc250-103">Interface ITablet2</span><span class="sxs-lookup"><span data-stu-id="dc250-103">ITablet2 interface</span></span>

<span data-ttu-id="dc250-104">Estende a [**interface ITablet**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="dc250-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="dc250-105">Membros</span><span class="sxs-lookup"><span data-stu-id="dc250-105">Members</span></span>

<span data-ttu-id="dc250-106">A interface **ITablet2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc250-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc250-107">**ITablet2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dc250-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="dc250-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc250-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc250-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc250-109">Methods</span></span>

<span data-ttu-id="dc250-110">A interface **ITablet2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dc250-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="dc250-111">Método</span><span class="sxs-lookup"><span data-stu-id="dc250-111">Method</span></span>                                          | <span data-ttu-id="dc250-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc250-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc250-113">**GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="dc250-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="dc250-114">Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.</span><span class="sxs-lookup"><span data-stu-id="dc250-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc250-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc250-115">Remarks</span></span>

<span data-ttu-id="dc250-116">Essa interface foi introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc250-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="dc250-117">Os desenvolvedores não devem usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="dc250-117">Developers should not use this interface.</span></span>

<span data-ttu-id="dc250-118">O código a seguir descreve como a interface **ITablet2** é definida.</span><span class="sxs-lookup"><span data-stu-id="dc250-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="dc250-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc250-119">Requirements</span></span>



| <span data-ttu-id="dc250-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc250-120">Requirement</span></span> | <span data-ttu-id="dc250-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dc250-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc250-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc250-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc250-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc250-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dc250-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc250-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc250-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dc250-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dc250-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc250-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="dc250-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc250-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

