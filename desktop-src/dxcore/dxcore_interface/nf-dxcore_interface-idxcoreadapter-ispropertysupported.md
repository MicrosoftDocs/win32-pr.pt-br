---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812420"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="5c7b7-103">Método IDXCoreAdapter:: IsPropertySupported</span><span class="sxs-lookup"><span data-stu-id="5c7b7-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="5c7b7-104">Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.</span><span class="sxs-lookup"><span data-stu-id="5c7b7-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c7b7-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="5c7b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c7b7-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="5c7b7-107">propriedade</span><span class="sxs-lookup"><span data-stu-id="5c7b7-107">property</span></span>

<span data-ttu-id="5c7b7-108">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="5c7b7-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="5c7b7-109">O tipo de propriedade que você está consultando sobre o suporte para.</span><span class="sxs-lookup"><span data-stu-id="5c7b7-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="5c7b7-110">Consulte a tabela em [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obter mais informações sobre cada propriedade de adaptador.</span><span class="sxs-lookup"><span data-stu-id="5c7b7-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="5c7b7-111">Retornos</span><span class="sxs-lookup"><span data-stu-id="5c7b7-111">Returns</span></span>

<span data-ttu-id="5c7b7-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="5c7b7-112">Type: **bool**</span></span>

<span data-ttu-id="5c7b7-113">Retorna  `true`   se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à propriedade de adaptador especificada.</span><span class="sxs-lookup"><span data-stu-id="5c7b7-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="5c7b7-114">Caso contrário, retorna  `false` .</span><span class="sxs-lookup"><span data-stu-id="5c7b7-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c7b7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c7b7-115">See also</span></span>

<span data-ttu-id="5c7b7-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="5c7b7-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>