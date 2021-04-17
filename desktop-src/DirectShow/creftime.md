---
description: A classe CReftime é uma classe auxiliar para gerenciar tempos de referência.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Classe CReftime (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748807"
---
# <a name="creftime-class"></a><span data-ttu-id="b1a12-103">Classe CReftime</span><span class="sxs-lookup"><span data-stu-id="b1a12-103">CRefTime class</span></span>

![hierarquia de classe CRefTime](images/cutil05.png)

<span data-ttu-id="b1a12-105">A `CRefTime` classe é uma classe auxiliar para gerenciar tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="b1a12-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="b1a12-106">Um *tempo de referência* é uma unidade de tempo representada em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b1a12-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="b1a12-107">Essa classe compartilha o mesmo layout de dados que o tipo de dados de [**\_ tempo de referência**](reference-time.md) , mas adiciona alguns métodos e operadores que fornecem funções de comparação, conversão e aritmética.</span><span class="sxs-lookup"><span data-stu-id="b1a12-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="b1a12-108">Para obter mais informações sobre os tempos de referência, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b1a12-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="b1a12-109">Variáveis de membro público</span><span class="sxs-lookup"><span data-stu-id="b1a12-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="b1a12-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1a12-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="b1a12-111">**\_tempo m**</span><span class="sxs-lookup"><span data-stu-id="b1a12-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="b1a12-112">Especifica o valor de **\_ tempo de referência** .</span><span class="sxs-lookup"><span data-stu-id="b1a12-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="b1a12-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="b1a12-113">Public Methods</span></span>                                                          | <span data-ttu-id="b1a12-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1a12-114">Description</span></span>                                           |
| [<span data-ttu-id="b1a12-115">**CReftime**</span><span class="sxs-lookup"><span data-stu-id="b1a12-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="b1a12-116">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="b1a12-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="b1a12-117">**Getunidades**</span><span class="sxs-lookup"><span data-stu-id="b1a12-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="b1a12-118">Recupera o tempo de referência em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b1a12-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="b1a12-119">**Milissegundos**</span><span class="sxs-lookup"><span data-stu-id="b1a12-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="b1a12-120">Converte o tempo de referência em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b1a12-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="b1a12-121">Operadores</span><span class="sxs-lookup"><span data-stu-id="b1a12-121">Operators</span></span>                                                               | <span data-ttu-id="b1a12-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1a12-122">Description</span></span>                                           |
| [<span data-ttu-id="b1a12-123">**\_tempo de referência do operador ()**</span><span class="sxs-lookup"><span data-stu-id="b1a12-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="b1a12-124">Converte o objeto em um tipo de dados de **\_ tempo de referência** .</span><span class="sxs-lookup"><span data-stu-id="b1a12-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="b1a12-125">**operador =**</span><span class="sxs-lookup"><span data-stu-id="b1a12-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="b1a12-126">Atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="b1a12-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="b1a12-127">**operador + =**</span><span class="sxs-lookup"><span data-stu-id="b1a12-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="b1a12-128">Adiciona dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="b1a12-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="b1a12-129">**operador =**</span><span class="sxs-lookup"><span data-stu-id="b1a12-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="b1a12-130">Subtrai um tempo de referência de outro.</span><span class="sxs-lookup"><span data-stu-id="b1a12-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b1a12-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1a12-131">Remarks</span></span>

<span data-ttu-id="b1a12-132">Há uma possível armadilha com o uso dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b1a12-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="b1a12-133">Se você aplicar o operador + = com um objeto **CRefTime** como o operando esquerdo e uma variável do tipo **Long** como operando à direita, o compilador irá forçar implicitamente o operando direito em um objeto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="b1a12-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="b1a12-134">Essa coerção usa o construtor **CRefTime** que converte milissegundos em \_ unidades de tempo de referência; como resultado, o operando à direita é multiplicado por 10.000:</span><span class="sxs-lookup"><span data-stu-id="b1a12-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="b1a12-135">No entanto, a mesma coisa não acontece usando o operador +:</span><span class="sxs-lookup"><span data-stu-id="b1a12-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="b1a12-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a12-136">Requirements</span></span>



| <span data-ttu-id="b1a12-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a12-137">Requirement</span></span> | <span data-ttu-id="b1a12-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a12-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a12-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1a12-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b1a12-140"><dt>REFTIME. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1a12-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1a12-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1a12-141">Library</span></span><br/> | <dl> <span data-ttu-id="b1a12-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b1a12-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




