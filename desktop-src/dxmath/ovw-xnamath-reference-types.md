---
description: A biblioteca DirectXMath fornece várias estruturas e tipos definidos para encapsular dados para dar suporte à facilidade de uso, otimização e portabilidade.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Tipos de biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827572"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="838d8-103">Tipos de biblioteca DirectXMath</span><span class="sxs-lookup"><span data-stu-id="838d8-103">DirectXMath Library types</span></span>

<span data-ttu-id="838d8-104">A biblioteca DirectXMath fornece várias estruturas e tipos definidos para encapsular dados para dar suporte à facilidade de uso, otimização e portabilidade.</span><span class="sxs-lookup"><span data-stu-id="838d8-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="838d8-105">A lista a seguir inclui estruturas que atualmente fazem parte da biblioteca DirectXMath e estão disponíveis por meio do cabeçalho DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="838d8-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="838d8-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="838d8-106">In this section</span></span>



| <span data-ttu-id="838d8-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="838d8-107">Topic</span></span>                                                             | <span data-ttu-id="838d8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="838d8-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="838d8-109">**MEIO tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="838d8-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="838d8-110">Um alias para **UInt16 \_ t** empacotado com um número de ponto flutuante de 16 bits que consiste em um bit de sinal, um expoente com tendência de 5 bits e um mantissa de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="838d8-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="838d8-111">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="838d8-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="838d8-112">Um tipo portátil usado para representar um vetor de ponto flutuante de 4 32 bits ou componentes inteiros, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.</span><span class="sxs-lookup"><span data-stu-id="838d8-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="838d8-113">**Tipo de dados XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="838d8-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="838d8-114">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores de ponto flutuante em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="838d8-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="838d8-115">**Tipo de dados XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="838d8-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="838d8-116">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores inteiros em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="838d8-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="838d8-117">**Tipo de dados XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="838d8-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="838d8-118">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores de t em uma instância de tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="838d8-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="838d8-119">**Tipo de dados XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="838d8-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="838d8-120">Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores t uint8 em uma instância do tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="838d8-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="838d8-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="838d8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="838d8-122">Referência de programação DirectXMath</span><span class="sxs-lookup"><span data-stu-id="838d8-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




