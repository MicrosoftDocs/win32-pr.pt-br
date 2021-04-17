---
description: O método GetFlags recupera os sinalizadores de contexto associados ao comando adiado.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Método CDeferredCommand. GetFlags (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770103"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="fc1db-103">Método CDeferredCommand. GetFlags</span><span class="sxs-lookup"><span data-stu-id="fc1db-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="fc1db-104">O `GetFlags` método recupera os sinalizadores de contexto associados ao comando adiado.</span><span class="sxs-lookup"><span data-stu-id="fc1db-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc1db-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="fc1db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc1db-106">Parameters</span></span>

<span data-ttu-id="fc1db-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc1db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc1db-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc1db-108">Return value</span></span>

<span data-ttu-id="fc1db-109">Retorna uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="fc1db-109">Returns one of the following:</span></span>



| <span data-ttu-id="fc1db-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fc1db-110">Return code</span></span>                                                                                             | <span data-ttu-id="fc1db-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc1db-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc1db-112"><dt>**método de expedição \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="fc1db-113">Execute o membro como um método.</span><span class="sxs-lookup"><span data-stu-id="fc1db-113">Run the member as a method.</span></span> <span data-ttu-id="fc1db-114">Se uma propriedade tiver o mesmo nome, isso e o \_ sinalizador PROPERTYGET de expedição poderão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="fc1db-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="fc1db-115"><dt>**PROPERTYGET de expedição \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="fc1db-116">O membro está sendo recuperado como uma propriedade ou um membro de dados.</span><span class="sxs-lookup"><span data-stu-id="fc1db-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="fc1db-117"><dt>**PROPERTYPUT de expedição \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="fc1db-118">O membro está sendo alterado como um membro de propriedade ou de dados.</span><span class="sxs-lookup"><span data-stu-id="fc1db-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="fc1db-119"><dt>**PROPERTYPUTREF de expedição \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="fc1db-120">O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor.</span><span class="sxs-lookup"><span data-stu-id="fc1db-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="fc1db-121">Esse sinalizador é válido somente quando a propriedade aceita uma referência a um objeto.</span><span class="sxs-lookup"><span data-stu-id="fc1db-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc1db-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc1db-122">Requirements</span></span>



| <span data-ttu-id="fc1db-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1db-123">Requirement</span></span> | <span data-ttu-id="fc1db-124">Valor</span><span class="sxs-lookup"><span data-stu-id="fc1db-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1db-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc1db-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fc1db-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc1db-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc1db-127">Library</span></span><br/> | <dl> <span data-ttu-id="fc1db-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fc1db-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1db-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc1db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1db-130">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="fc1db-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




