---
title: DirectXMath numéricos e APIs de interoperabilidade do Windows (Windowsnumerics. h)
description: Essas funções convertem os tipos Windows. Foundation. Numerics de e para os tipos DirectXMath SIMD XMVECTOR e XMMATRIX.
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- APIs de interoperabilidade DirectXMath e numéricas do Windows
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780737"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="d0ce0-104">APIs de interoperabilidade DirectXMath e numéricas do Windows</span><span class="sxs-lookup"><span data-stu-id="d0ce0-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="d0ce0-105">Essas funções convertem os tipos [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) de e para os tipos DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) e [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="d0ce0-106">Funções</span><span class="sxs-lookup"><span data-stu-id="d0ce0-106">Functions</span></span>

| <span data-ttu-id="d0ce0-107">Nome</span><span class="sxs-lookup"><span data-stu-id="d0ce0-107">Name</span></span> | <span data-ttu-id="d0ce0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0ce0-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="d0ce0-109">Carrega um float2 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="d0ce0-110">Carrega um float3 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="d0ce0-111">Carrega um FLOAT4 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="d0ce0-112">Carrega um float3x2 em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="d0ce0-113">Carrega um float4x4 em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="d0ce0-114">Carrega um plano em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="d0ce0-115">Carrega um Quaternion em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span><span class="sxs-lookup"><span data-stu-id="d0ce0-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="d0ce0-116">Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um float2.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="d0ce0-117">Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um float3.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="d0ce0-118">Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="d0ce0-119">Armazena um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) em um float3x2.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="d0ce0-120">Armazena um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) em um float4x4.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="d0ce0-121">Armazena um [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath em um plano.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="d0ce0-122">Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0ce0-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d0ce0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ce0-123">Requirements</span></span>

| <span data-ttu-id="d0ce0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ce0-124">Requirement</span></span> | <span data-ttu-id="d0ce0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ce0-125">Value</span></span> |
|-|-|
| <span data-ttu-id="d0ce0-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0ce0-126">Namespace</span></span> | <span data-ttu-id="d0ce0-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="d0ce0-127">DirectX</span></span> |
| <span data-ttu-id="d0ce0-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0ce0-128">Header</span></span> | <dl> <span data-ttu-id="d0ce0-129"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ce0-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d0ce0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ce0-130">See also</span></span>

[<span data-ttu-id="d0ce0-131">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="d0ce0-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
