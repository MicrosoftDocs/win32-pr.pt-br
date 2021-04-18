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
# <a name="windows-numerics-and-directxmath-interop-apis"></a>APIs de interoperabilidade DirectXMath e numéricas do Windows

Essas funções convertem os tipos [**Windows. Foundation. Numerics**](/uwp/api/Windows.Foundation.Numerics) de e para os tipos DirectXMath SIMD [XMVECTOR](../dxmath/xmvector-data-type.md) e [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | Carrega um float2 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | Carrega um float3 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md). |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | Carrega um FLOAT4 em um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md). |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | Carrega um float3x2 em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | Carrega um float4x4 em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | Carrega um plano em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | Carrega um Quaternion em um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix). |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um float2. |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um float3. |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um FLOAT4. |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | Armazena um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) em um float3x2. |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | Armazena um DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) em um float4x4. |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | Armazena um [XMVECTOR](../dxmath/xmvector-data-type.md) DirectXMath em um plano. |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | Armazena um DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) em um Quaternion. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | DirectX |
| parâmetro | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
