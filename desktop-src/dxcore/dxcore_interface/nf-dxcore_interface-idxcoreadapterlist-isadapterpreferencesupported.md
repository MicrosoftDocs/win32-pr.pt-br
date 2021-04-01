---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina se um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado é compreendido pelo sistema operacional.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641284"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="9337f-103">Método IDXCoreAdapterList:: IsAdapterPreferenceSupported</span><span class="sxs-lookup"><span data-stu-id="9337f-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="9337f-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="9337f-104">Description</span></span>

<span data-ttu-id="9337f-105">Determina se um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) especificado é compreendido pelo sistema operacional atual (SO).</span><span class="sxs-lookup"><span data-stu-id="9337f-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="9337f-106">Você pode chamar **IsAdapterPreferenceSupported** antes de chamar [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="9337f-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9337f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9337f-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="9337f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9337f-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="9337f-109">preferência</span><span class="sxs-lookup"><span data-stu-id="9337f-109">preference</span></span>

<span data-ttu-id="9337f-110">Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="9337f-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="9337f-111">Um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) que será verificado para ver se há suporte pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9337f-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="9337f-112">Retornos</span><span class="sxs-lookup"><span data-stu-id="9337f-112">Returns</span></span>

<span data-ttu-id="9337f-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="9337f-113">Type: **bool**</span></span>

<span data-ttu-id="9337f-114">Retorna `true` se o tipo de classificação é compreendido pelo sistema operacional atual.</span><span class="sxs-lookup"><span data-stu-id="9337f-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="9337f-115">Caso contrário, retorna `false`.</span><span class="sxs-lookup"><span data-stu-id="9337f-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9337f-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="9337f-116">See also</span></span>

<span data-ttu-id="9337f-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9337f-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>