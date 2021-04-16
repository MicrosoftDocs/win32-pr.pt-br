---
description: A classe COARefTime converte os tempos de referência entre as unidades de segundos e 100-nanossegundos.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Classe COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758693"
---
# <a name="coareftime-class"></a><span data-ttu-id="b704f-103">Classe COARefTime</span><span class="sxs-lookup"><span data-stu-id="b704f-103">COARefTime class</span></span>

![hierarquia de classe COARefTime](images/cutil05.png)

<span data-ttu-id="b704f-105">A `COARefTime` classe converte os tempos de referência entre as unidades de segundos e 100-nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b704f-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="b704f-106">Essa classe é convertida entre os tempos de referência que são compatíveis com a automação e os tempos de referência que são compatíveis com C/C++.</span><span class="sxs-lookup"><span data-stu-id="b704f-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="b704f-107">Interfaces compatíveis com automação usam valores **duplos** para representar o tempo em segundos.</span><span class="sxs-lookup"><span data-stu-id="b704f-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="b704f-108">Outras interfaces usam valores **LONGLONG** de 64 bits para representar o tempo em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b704f-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="b704f-109">Os seguintes tipos são definidos para esses valores:</span><span class="sxs-lookup"><span data-stu-id="b704f-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="b704f-110">Os filtros podem usar a `COARefTime` classe para converter entre os dois formatos.</span><span class="sxs-lookup"><span data-stu-id="b704f-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="b704f-111">Essa classe é derivada da classe [**CRefTime**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b704f-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="b704f-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="b704f-112">Public Methods</span></span>                                          | <span data-ttu-id="b704f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b704f-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b704f-114">**COARefTime**</span><span class="sxs-lookup"><span data-stu-id="b704f-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="b704f-115">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="b704f-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="b704f-116">Operadores</span><span class="sxs-lookup"><span data-stu-id="b704f-116">Operators</span></span>                                               | <span data-ttu-id="b704f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b704f-117">Description</span></span>                                                           |
| [<span data-ttu-id="b704f-118">**double**</span><span class="sxs-lookup"><span data-stu-id="b704f-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="b704f-119">Converte o tempo de referência em um valor **duplo** .</span><span class="sxs-lookup"><span data-stu-id="b704f-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="b704f-120">**hora de referência \_**</span><span class="sxs-lookup"><span data-stu-id="b704f-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="b704f-121">Converte o objeto em um valor **de \_ tempo de referência** .</span><span class="sxs-lookup"><span data-stu-id="b704f-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="b704f-122">**operador =**</span><span class="sxs-lookup"><span data-stu-id="b704f-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="b704f-123">Atribui um novo tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="b704f-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="b704f-124">**operador = =**</span><span class="sxs-lookup"><span data-stu-id="b704f-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="b704f-125">Testes de igualdade entre dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="b704f-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="b704f-126">**operador! =**</span><span class="sxs-lookup"><span data-stu-id="b704f-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="b704f-127">Testa desigualdade entre dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="b704f-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="b704f-128">**<do operador**</span><span class="sxs-lookup"><span data-stu-id="b704f-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="b704f-129">Testa se um tempo de referência é menor que o outro.</span><span class="sxs-lookup"><span data-stu-id="b704f-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="b704f-130">**>do operador**</span><span class="sxs-lookup"><span data-stu-id="b704f-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="b704f-131">Testa se um tempo de referência é maior que o outro.</span><span class="sxs-lookup"><span data-stu-id="b704f-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="b704f-132">**<do operador =**</span><span class="sxs-lookup"><span data-stu-id="b704f-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="b704f-133">Testa se um tempo de referência é menor ou igual a outro.</span><span class="sxs-lookup"><span data-stu-id="b704f-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="b704f-134">**>do operador =**</span><span class="sxs-lookup"><span data-stu-id="b704f-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="b704f-135">Testa se um tempo de referência é maior ou igual a outro.</span><span class="sxs-lookup"><span data-stu-id="b704f-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="b704f-136">**operador +**</span><span class="sxs-lookup"><span data-stu-id="b704f-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="b704f-137">Adiciona dois tempos de referência.</span><span class="sxs-lookup"><span data-stu-id="b704f-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="b704f-138">\* \* operador \* \*</span><span class="sxs-lookup"><span data-stu-id="b704f-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="b704f-139">Subtrai um tempo de referência de outro.</span><span class="sxs-lookup"><span data-stu-id="b704f-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="b704f-140">**operador + =**</span><span class="sxs-lookup"><span data-stu-id="b704f-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="b704f-141">Adiciona dois tempos de referência e atribui o resultado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b704f-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="b704f-142">**operador =**</span><span class="sxs-lookup"><span data-stu-id="b704f-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="b704f-143">Subtrai dois tempos de referência e atribui o resultado a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b704f-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="b704f-144">**operador \***</span><span class="sxs-lookup"><span data-stu-id="b704f-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="b704f-145">Multiplica um tempo de referência por um valor.</span><span class="sxs-lookup"><span data-stu-id="b704f-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="b704f-146">**operador**</span><span class="sxs-lookup"><span data-stu-id="b704f-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="b704f-147">Divide um tempo de referência por um valor.</span><span class="sxs-lookup"><span data-stu-id="b704f-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="b704f-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b704f-148">Requirements</span></span>



| <span data-ttu-id="b704f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b704f-149">Requirement</span></span> | <span data-ttu-id="b704f-150">Valor</span><span class="sxs-lookup"><span data-stu-id="b704f-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b704f-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b704f-151">Header</span></span><br/>  | <dl> <span data-ttu-id="b704f-152"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b704f-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b704f-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b704f-153">Library</span></span><br/> | <dl> <span data-ttu-id="b704f-154"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b704f-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




