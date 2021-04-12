---
title: DXCoreAdapterPreference
description: Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366442"
---
# <a name="dxcoreadapterpreference-enum"></a><span data-ttu-id="2435b-103">DXCoreAdapterPreference enum</span><span class="sxs-lookup"><span data-stu-id="2435b-103">DXCoreAdapterPreference enum</span></span>

## <a name="description"></a><span data-ttu-id="2435b-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="2435b-104">Description</span></span>

<span data-ttu-id="2435b-105">Define constantes que especificam as preferências do adaptador DXCore a serem usadas como critérios de classificação de lista.</span><span class="sxs-lookup"><span data-stu-id="2435b-105">Defines constants that specify DXCore adapter preferences to be used as list-sorting criteria.</span></span> <span data-ttu-id="2435b-106">Você pode classificar uma lista de adaptadores DXCore passando uma matriz de **DXCoreAdapterPreference** para [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span><span class="sxs-lookup"><span data-stu-id="2435b-106">You can sort a DXCore adapter list by passing an array of **DXCoreAdapterPreference** to [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2435b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2435b-107">Syntax</span></span>

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a><span data-ttu-id="2435b-108">Campos de enumeração</span><span class="sxs-lookup"><span data-stu-id="2435b-108">Enum fields</span></span>

### <a name="hardware"></a><span data-ttu-id="2435b-109">Hardware</span><span class="sxs-lookup"><span data-stu-id="2435b-109">Hardware</span></span>

<span data-ttu-id="2435b-110">Especifica uma preferência para adaptadores de hardware (em oposição aos adaptadores de software).</span><span class="sxs-lookup"><span data-stu-id="2435b-110">Specifies a preference for hardware adapters (as opposed to software adapters).</span></span>

### <a name="minimumpower"></a><span data-ttu-id="2435b-111">MinimumPower</span><span class="sxs-lookup"><span data-stu-id="2435b-111">MinimumPower</span></span>

<span data-ttu-id="2435b-112">Especifica uma preferência para a GPU com capacidade mínima (como um processador gráfico integrado ou iGPU).</span><span class="sxs-lookup"><span data-stu-id="2435b-112">Specifies a preference for the minimum-powered GPU (such as an integrated graphics processor, or iGPU).</span></span>

### <a name="highperformance"></a><span data-ttu-id="2435b-113">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="2435b-113">HighPerformance</span></span>

<span data-ttu-id="2435b-114">Especifica uma preferência para a GPU de alto desempenho, como um processador gráfico externo (xGPU), se disponível, ou dGPU (processador gráfico discreto), se disponível.</span><span class="sxs-lookup"><span data-stu-id="2435b-114">Specifies a preference for the highest-performance GPU, such as an external graphics processor (xGPU), if available, or discrete graphics processor (dGPU) if available.</span></span>

## <a name="see-also"></a><span data-ttu-id="2435b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2435b-115">See also</span></span>

<span data-ttu-id="2435b-116">[IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="2435b-116">[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>