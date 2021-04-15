---
description: Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores de ponto flutuante em uma instância do tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo de dados XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747457"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="ffb1f-103">Tipo de dados XMVECTORF32</span><span class="sxs-lookup"><span data-stu-id="ffb1f-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="ffb1f-104">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores de ponto flutuante em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb1f-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="ffb1f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffb1f-105">Remarks</span></span>

<span data-ttu-id="ffb1f-106">Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando `XMVECTORF32` ao programar em C++, consulte [extensões de XMVECTORF32](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ffb1f-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="ffb1f-107">As estruturas **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) são fornecidas como um mecanismo para criar [**XMVECTOR**](xmvector-data-type.md) de tipos de dados constantes diferentes (ponto flutuante, inteiro sem sinal, inteiro e byte) usando inicializadores.</span><span class="sxs-lookup"><span data-stu-id="ffb1f-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="ffb1f-108">Isso é necessário para dar suporte a [**XMVECTOR**](xmvector-data-type.md), pois ele não oferece suporte a inicializadores, por motivos de portabilidade e otimização.</span><span class="sxs-lookup"><span data-stu-id="ffb1f-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="ffb1f-109">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ffb1f-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="ffb1f-110">**Namespace**: usar DirectX</span><span class="sxs-lookup"><span data-stu-id="ffb1f-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ffb1f-111">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="ffb1f-111">Platform Requirements</span></span>

<span data-ttu-id="ffb1f-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ffb1f-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ffb1f-113">Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ffb1f-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb1f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffb1f-114">Requirements</span></span>



| <span data-ttu-id="ffb1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb1f-115">Requirement</span></span> | <span data-ttu-id="ffb1f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ffb1f-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb1f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffb1f-117">Header</span></span><br/> | <dl> <span data-ttu-id="ffb1f-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb1f-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb1f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffb1f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb1f-120">Tipos de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ffb1f-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="ffb1f-121">**Tipo de dados XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="ffb1f-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ffb1f-122">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="ffb1f-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="ffb1f-123">**Tipo de dados XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="ffb1f-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ffb1f-124">**Tipo de dados XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="ffb1f-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="ffb1f-125">**Tipo de dados XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="ffb1f-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 




