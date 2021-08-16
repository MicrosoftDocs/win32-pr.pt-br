---
description: O método CBaseList implementa uma lista abtract. O modelo de classe CGenericList, que deriva de CBaseList, fornece verificação de tipo e uma interface mais simples do que a classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Classe CBaseList (Wxlist.h)
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
ms.openlocfilehash: 5616edd16921bb2ae4d1a0b7ad67f5bbec3fba560594d4710512bd2cec6f275f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823697"
---
# <a name="cbaselist-class"></a>Classe CBaseList

![Hierarquia de classes cbaselist](images/list01.png)

O **método CBaseList** implementa uma lista abtract. O [**modelo de classe CGenericList,**](cgenericlist.md) que deriva de **CBaseList,** fornece verificação de tipo e uma interface mais simples do que a **classe CBaseList.**

A **classe CBaseList** é modelada após a **classe CObList** na biblioteca MFC (MFC). As posições dentro da lista são representadas por uma estrutura POSITION. O chamador não deve acessar os membros internos da estrutura POSITION; tratá-lo como um ponteiro para um nó de lista. A posição de um objeto na lista permanece válida até que o objeto seja excluído.

A lista não requer suporte pelos objetos que ela contém. Ele não executa nenhum gerenciamento de armazenamento ou cópia nos objetos. Os objetos podem estar em várias listas.

Aproximadamente metade dos métodos nesta classe atuam em objetos individuais. Esses métodos têm o sufixo – I no nome do método. Os outros métodos atuam em listas inteiras. Por exemplo, o [**método CBaseList::AddAfter**](cbaselist-addafter.md) acrescenta uma lista a outra lista. As operações de objeto único retornam valores POSITION ou **NULL** em caso de falha. As operações de lista **retornarão TRUE** se for bem-sucedida ou **FALSE caso** contrário.



| Variáveis de membro protegidas                             | Descrição                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**m \_ Count**](cbaselist-m-count.md)                  | Número de itens na lista.                                              |
| [**m \_ pFirst**](cbaselist-m-pfirst.md)                | Ponteiro para o primeiro nó na lista.                                    |
| [**m \_ pLast**](cbaselist-m-plast.md)                  | Ponteiro para o último nó na lista.                                     |
| Métodos Protegidos                                      | Descrição                                                               |
| [**GetNextI**](cbaselist-getnexti.md)                 | Recupera o item na posição especificada e avança a posição.  |
| [**GetI**](cbaselist-geti.md)                         | Recupera o item na posição especificada.                             |
| [**FindI**](cbaselist-findi.md)                       | Recupera a primeira posição que contém o item especificado.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Remove o primeiro item na lista.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Remove o último item na lista.                                        |
| [**RemoveI**](cbaselist-removei.md)                   | Remove o item na posição especificada.                               |
| [**AddTailI**](cbaselist-addtaili.md)                 | Adiciona um item ao final da lista.                                      |
| [**AddHeadI**](cbaselist-addheadi.md)                 | Adiciona um item à frente da lista.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Insere um item após a posição especificada.                             |
| [**AddBeforeI**](cbaselist-addbeforei.md)             | Insere um item antes da posição especificada.                            |
| Métodos públicos                                         | Descrição                                                               |
| [**Cbaselist**](cbaselist-cbaselist.md)               | Método do construtor.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Método destruidor.                                                        |
| [**Removeall**](cbaselist-removeall.md)               | Remove todos os nós da lista.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Recupera a posição do primeiro item na lista.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Recupera a posição do último item da lista.                      |
| [**GetCountI**](cbaselist-getcounti.md)               | Recupera o número de itens na lista.                                |
| [**Avançar**](cbaselist-next.md)                         | Recupera a próxima posição na lista.                                  |
| [**Prev**](cbaselist-prev.md)                         | Recupera a posição anterior na lista.                              |
| [**Addhead**](cbaselist-addhead.md)                   | Insere outra lista na frente desta lista.                           |
| [**Addtail**](cbaselist-addtail.md)                   | Anexa outra lista ao final desta lista.                             |
| [**Addafter**](cbaselist-addafter.md)                 | Insere uma lista após a posição especificada.                              |
| [**Addbefore**](cbaselist-addbefore.md)               | Insere uma lista antes da posição especificada.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Divide a lista e anexa a parte de cabeça à parte final de outra lista. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Divide a lista e insere a parte final na parte superior de outra lista. |
| [**Reverter**](cbaselist-reverse.md)                   | Inverte a ordem da lista.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Base Classes](directshow-base-classes.md)
</dt> </dl>

 

 




