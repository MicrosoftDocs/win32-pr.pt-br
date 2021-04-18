---
description: A classe CBaseObject é uma classe abstrata para implementar objetos DirectShow. Para implementar objetos COM Component Object Model (COM), use a classe CUnknown, que deriva de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Classe CBaseObject (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770298"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="df5fe-104">Classe CBaseObject</span><span class="sxs-lookup"><span data-stu-id="df5fe-104">CBaseObject class</span></span>

<span data-ttu-id="df5fe-105">A classe **CBaseObject** é uma classe abstrata para implementar objetos DirectShow.</span><span class="sxs-lookup"><span data-stu-id="df5fe-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="df5fe-106">Para implementar objetos COM Component Object Model (COM), use a classe [**CUnknown**](cunknown.md) , que deriva de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="df5fe-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="df5fe-107">Métodos de classe</span><span class="sxs-lookup"><span data-stu-id="df5fe-107">Class Methods</span></span>                                      | <span data-ttu-id="df5fe-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="df5fe-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="df5fe-109">**CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="df5fe-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="df5fe-110">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="df5fe-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="df5fe-111">**~ CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="df5fe-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="df5fe-112">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="df5fe-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="df5fe-113">**ObjectsActive**</span><span class="sxs-lookup"><span data-stu-id="df5fe-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="df5fe-114">Recupera a contagem de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="df5fe-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="df5fe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="df5fe-115">Remarks</span></span>

<span data-ttu-id="df5fe-116">A maioria das classes base do DirectShow deriva de **CBaseObject**.</span><span class="sxs-lookup"><span data-stu-id="df5fe-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="df5fe-117">Essa classe fornece assistência de depuração mantendo uma contagem de todos os objetos do DirectShow ativos durante o tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="df5fe-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="df5fe-118">A contagem de objetos é armazenada em uma variável de membro de classe estática:</span><span class="sxs-lookup"><span data-stu-id="df5fe-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="df5fe-119">Em compilações de depuração, a DLL será declarada se for descarregada enquanto a contagem de objetos for maior que zero.</span><span class="sxs-lookup"><span data-stu-id="df5fe-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="df5fe-120">Isso torna mais fácil rastrear vazamentos causados por problemas de contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="df5fe-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="df5fe-121">O construtor **CBaseObject** Obtém um argumento, um nome de depuração para o objeto.</span><span class="sxs-lookup"><span data-stu-id="df5fe-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="df5fe-122">Esse nome é armazenado em uma tabela global na DLL.</span><span class="sxs-lookup"><span data-stu-id="df5fe-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="df5fe-123">A função [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) formata uma lista dos objetos ativos na dll e a envia para a saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="df5fe-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="df5fe-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df5fe-124">Requirements</span></span>



| <span data-ttu-id="df5fe-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="df5fe-125">Requirement</span></span> | <span data-ttu-id="df5fe-126">Valor</span><span class="sxs-lookup"><span data-stu-id="df5fe-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df5fe-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df5fe-127">Header</span></span><br/>  | <dl> <span data-ttu-id="df5fe-128"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df5fe-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df5fe-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df5fe-129">Library</span></span><br/> | <dl> <span data-ttu-id="df5fe-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="df5fe-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df5fe-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="df5fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5fe-132">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="df5fe-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




