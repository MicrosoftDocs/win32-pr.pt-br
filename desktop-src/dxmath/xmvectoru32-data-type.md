---
description: Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores de t em uma instância de tipo XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Tipo de dados XMVECTORU32 (Directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786202"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="d3d98-103">Tipo de dados XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="d3d98-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="d3d98-104">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores de t em uma instância de tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d98-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="d3d98-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3d98-105">Remarks</span></span>

<span data-ttu-id="d3d98-106">Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando XMVECTORU32 ao programar em C++, consulte [extensões de XMVECTORU32](ovw-xmvectoru32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="d3d98-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="d3d98-107">As estruturas [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) são fornecidas como um mecanismo para criar [**XMVECTOR**](xmvector-data-type.md) de tipos de dados constantes diferentes (ponto flutuante, inteiro sem sinal, inteiro e byte) usando inicializadores.</span><span class="sxs-lookup"><span data-stu-id="d3d98-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="d3d98-108">Isso é necessário para dar suporte a [**XMVECTOR**](xmvector-data-type.md), pois ele não oferece suporte a inicializadores, por motivos de portabilidade e otimização.</span><span class="sxs-lookup"><span data-stu-id="d3d98-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="d3d98-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d3d98-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="d3d98-110">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="d3d98-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="d3d98-111">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="d3d98-111">Platform Requirements</span></span>

<span data-ttu-id="d3d98-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3d98-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="d3d98-113">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="d3d98-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d98-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d98-114">Requirements</span></span>



| <span data-ttu-id="d3d98-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d98-115">Requirement</span></span> | <span data-ttu-id="d3d98-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d3d98-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d98-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3d98-117">Header</span></span><br/> | <dl> <span data-ttu-id="d3d98-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d98-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d98-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3d98-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d98-120">Tipos de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="d3d98-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="d3d98-121">**Tipo de dados XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="d3d98-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="d3d98-122">**Tipo de dados XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="d3d98-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="d3d98-123">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="d3d98-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="d3d98-124">**Tipo de dados XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="d3d98-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="d3d98-125">Extensões XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="d3d98-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




