---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366158"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="ce4db-103">Método IDXCoreAdapter:: IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="ce4db-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="ce4db-104">Determina se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="ce4db-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce4db-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="ce4db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="ce4db-107">attributeGUID</span><span class="sxs-lookup"><span data-stu-id="ce4db-107">attributeGUID</span></span>

<span data-ttu-id="ce4db-108">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">Type: **REFGUID**</span></span>

<span data-ttu-id="ce4db-109">Uma referência a um GUID de atributo de adaptador.</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="ce4db-110">Para obter uma lista de GUIDs de atributo, consulte [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="ce4db-111">Retornos</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">Returns</span></span>

<span data-ttu-id="ce4db-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="ce4db-112">Type: **bool**</span></span>

<span data-ttu-id="ce4db-113">Retorna  `true`   se este objeto de adaptador DXCore dá suporte ao atributo de adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="ce4db-114">Caso contrário, retorna  `false` .</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce4db-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">See also</span></span>

<span data-ttu-id="ce4db-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ce4db-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>