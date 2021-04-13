---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à definição do valor do estado do adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366441"
---
# <a name="idxcoreadapterissetstatesupported-method"></a><span data-ttu-id="7f9da-103">Método IDXCoreAdapter:: IsSetStateSupported</span><span class="sxs-lookup"><span data-stu-id="7f9da-103">IDXCoreAdapter::IsSetStateSupported method</span></span>

<span data-ttu-id="7f9da-104">Determina se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à definição do valor do estado do adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f9da-104">Determines whether this DXCore adapter object and the current operating system (OS) support setting the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f9da-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="7f9da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f9da-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="7f9da-107">state</span><span class="sxs-lookup"><span data-stu-id="7f9da-107">state</span></span>

<span data-ttu-id="7f9da-108">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="7f9da-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="7f9da-109">O tipo de item de estado que você está consultando sobre o suporte para.</span><span class="sxs-lookup"><span data-stu-id="7f9da-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="7f9da-110">Consulte a tabela em [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obter mais informações sobre cada tipo de estado de adaptador.</span><span class="sxs-lookup"><span data-stu-id="7f9da-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="7f9da-111">Retornos</span><span class="sxs-lookup"><span data-stu-id="7f9da-111">Returns</span></span>

<span data-ttu-id="7f9da-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="7f9da-112">Type: **bool**</span></span>

<span data-ttu-id="7f9da-113">Retorna  `true`   se este objeto de adaptador DXCore e o sistema operacional atual (SO) dão suporte à configuração do estado do adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="7f9da-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support setting the specified adapter state.</span></span> <span data-ttu-id="7f9da-114">Caso contrário, retorna  `false` .</span><span class="sxs-lookup"><span data-stu-id="7f9da-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f9da-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f9da-115">See also</span></span>

<span data-ttu-id="7f9da-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7f9da-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>