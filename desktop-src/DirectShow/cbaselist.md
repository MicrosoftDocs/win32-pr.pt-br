---
description: O método CBaseList implementa uma lista abtract. O modelo de classe CGenericList, que deriva de CBaseList, fornece verificação de tipo e uma interface mais simples do que a classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Classe CBaseList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778639"
---
# <a name="cbaselist-class"></a><span data-ttu-id="fb83f-104">Classe CBaseList</span><span class="sxs-lookup"><span data-stu-id="fb83f-104">CBaseList class</span></span>

![hierarquia de classe CBaseList](images/list01.png)

<span data-ttu-id="fb83f-106">O método **CBaseList** implementa uma lista abtract.</span><span class="sxs-lookup"><span data-stu-id="fb83f-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="fb83f-107">O modelo de classe [**CGenericList**](cgenericlist.md) , que deriva de **CBaseList**, fornece verificação de tipo e uma interface mais simples do que a classe **CBaseList** .</span><span class="sxs-lookup"><span data-stu-id="fb83f-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="fb83f-108">A classe **CBaseList** é modelada após a classe **CObList** na biblioteca MFC (MFC).</span><span class="sxs-lookup"><span data-stu-id="fb83f-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="fb83f-109">As posições dentro da lista são representadas por uma estrutura de posição.</span><span class="sxs-lookup"><span data-stu-id="fb83f-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="fb83f-110">O chamador não deve acessar os membros internos da estrutura de posição; tratá-lo como um ponteiro para um nó de lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="fb83f-111">A posição de um objeto na lista permanece válida até que o objeto seja excluído.</span><span class="sxs-lookup"><span data-stu-id="fb83f-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="fb83f-112">A lista não requer nenhum suporte dos objetos que ele contém.</span><span class="sxs-lookup"><span data-stu-id="fb83f-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="fb83f-113">Ele não realiza nenhum gerenciamento de armazenamento nem cópia nos objetos.</span><span class="sxs-lookup"><span data-stu-id="fb83f-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="fb83f-114">Os objetos podem estar em várias listas.</span><span class="sxs-lookup"><span data-stu-id="fb83f-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="fb83f-115">Aproximadamente metade dos métodos nessa classe atuam em objetos únicos.</span><span class="sxs-lookup"><span data-stu-id="fb83f-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="fb83f-116">Esses métodos têm o sufixo-I no nome do método.</span><span class="sxs-lookup"><span data-stu-id="fb83f-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="fb83f-117">Os outros métodos agem em listas inteiras.</span><span class="sxs-lookup"><span data-stu-id="fb83f-117">The other methods act on entire lists.</span></span> <span data-ttu-id="fb83f-118">Por exemplo, o método [**CBaseList:: AddAfter**](cbaselist-addafter.md) anexa uma lista a outra lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="fb83f-119">Operações de objeto único retornam valores de posição ou **NULL** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="fb83f-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="fb83f-120">As operações de lista retornarão **true** se for bem-sucedido ou **false** .</span><span class="sxs-lookup"><span data-stu-id="fb83f-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="fb83f-121">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="fb83f-121">Protected Member Variables</span></span>                             | <span data-ttu-id="fb83f-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb83f-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fb83f-123">**contagem de m \_**</span><span class="sxs-lookup"><span data-stu-id="fb83f-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="fb83f-124">Número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="fb83f-125">**\_pFirst m**</span><span class="sxs-lookup"><span data-stu-id="fb83f-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="fb83f-126">Ponteiro para o primeiro nó na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="fb83f-127">**\_pLast m**</span><span class="sxs-lookup"><span data-stu-id="fb83f-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="fb83f-128">Ponteiro para o último nó na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="fb83f-129">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="fb83f-129">Protected Methods</span></span>                                      | <span data-ttu-id="fb83f-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb83f-130">Description</span></span>                                                               |
| [<span data-ttu-id="fb83f-131">**Getpróximoi**</span><span class="sxs-lookup"><span data-stu-id="fb83f-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="fb83f-132">Recupera o item na posição especificada e avança a posição.</span><span class="sxs-lookup"><span data-stu-id="fb83f-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="fb83f-133">**GetI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="fb83f-134">Recupera o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="fb83f-135">**Localizar**</span><span class="sxs-lookup"><span data-stu-id="fb83f-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="fb83f-136">Recupera a primeira posição que contém o item especificado.</span><span class="sxs-lookup"><span data-stu-id="fb83f-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="fb83f-137">**RemoveHeadI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="fb83f-138">Remove o primeiro item da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="fb83f-139">**RemoveTailI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="fb83f-140">Remove o último item da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="fb83f-141">**Mover para**</span><span class="sxs-lookup"><span data-stu-id="fb83f-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="fb83f-142">Remove o item na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="fb83f-143">**Addcaudai**</span><span class="sxs-lookup"><span data-stu-id="fb83f-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="fb83f-144">Adiciona um item ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="fb83f-145">**Subtítuloi**</span><span class="sxs-lookup"><span data-stu-id="fb83f-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="fb83f-146">Adiciona um item à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="fb83f-147">**AddAfterI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="fb83f-148">Insere um item após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="fb83f-149">**Addantes de**</span><span class="sxs-lookup"><span data-stu-id="fb83f-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="fb83f-150">Insere um item antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="fb83f-151">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="fb83f-151">Public Methods</span></span>                                         | <span data-ttu-id="fb83f-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb83f-152">Description</span></span>                                                               |
| [<span data-ttu-id="fb83f-153">**CBaseList**</span><span class="sxs-lookup"><span data-stu-id="fb83f-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="fb83f-154">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="fb83f-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="fb83f-155">**~ CBaseList**</span><span class="sxs-lookup"><span data-stu-id="fb83f-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="fb83f-156">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="fb83f-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="fb83f-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="fb83f-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="fb83f-158">Remove todos os nós da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="fb83f-159">**GetHeadPositionI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="fb83f-160">Recupera a posição do primeiro item na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="fb83f-161">**GetTailPositionI**</span><span class="sxs-lookup"><span data-stu-id="fb83f-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="fb83f-162">Recupera a posição do último item da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="fb83f-163">**Getcounteri**</span><span class="sxs-lookup"><span data-stu-id="fb83f-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="fb83f-164">Recupera o número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="fb83f-165">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="fb83f-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="fb83f-166">Recupera a próxima posição na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="fb83f-167">**/S**</span><span class="sxs-lookup"><span data-stu-id="fb83f-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="fb83f-168">Recupera a posição anterior na lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="fb83f-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="fb83f-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="fb83f-170">Insere outra lista na frente desta lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="fb83f-171">**Addcaudal**</span><span class="sxs-lookup"><span data-stu-id="fb83f-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="fb83f-172">Acrescenta outra lista ao final desta lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="fb83f-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="fb83f-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="fb83f-174">Insere uma lista após a posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="fb83f-175">**Addantes**</span><span class="sxs-lookup"><span data-stu-id="fb83f-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="fb83f-176">Insere uma lista antes da posição especificada.</span><span class="sxs-lookup"><span data-stu-id="fb83f-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="fb83f-177">**MoveToTail**</span><span class="sxs-lookup"><span data-stu-id="fb83f-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="fb83f-178">Divide a lista e acrescenta a parte de cabeçalho à cauda de outra lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="fb83f-179">**MoveToHead**</span><span class="sxs-lookup"><span data-stu-id="fb83f-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="fb83f-180">Divide a lista e insere a parte final no cabeçalho de outra lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="fb83f-181">**Ordem**</span><span class="sxs-lookup"><span data-stu-id="fb83f-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="fb83f-182">Inverte a ordem da lista.</span><span class="sxs-lookup"><span data-stu-id="fb83f-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="fb83f-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb83f-183">Requirements</span></span>



| <span data-ttu-id="fb83f-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb83f-184">Requirement</span></span> | <span data-ttu-id="fb83f-185">Valor</span><span class="sxs-lookup"><span data-stu-id="fb83f-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb83f-186">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb83f-186">Header</span></span><br/>  | <dl> <span data-ttu-id="fb83f-187"><dt>Wxlist. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb83f-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fb83f-188">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb83f-188">Library</span></span><br/> | <dl> <span data-ttu-id="fb83f-189"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fb83f-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb83f-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb83f-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb83f-191">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb83f-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




