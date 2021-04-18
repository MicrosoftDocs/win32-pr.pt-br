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
# <a name="cbaselist-class"></a>Classe CBaseList

![hierarquia de classe CBaseList](images/list01.png)

O método **CBaseList** implementa uma lista abtract. O modelo de classe [**CGenericList**](cgenericlist.md) , que deriva de **CBaseList**, fornece verificação de tipo e uma interface mais simples do que a classe **CBaseList** .

A classe **CBaseList** é modelada após a classe **CObList** na biblioteca MFC (MFC). As posições dentro da lista são representadas por uma estrutura de posição. O chamador não deve acessar os membros internos da estrutura de posição; tratá-lo como um ponteiro para um nó de lista. A posição de um objeto na lista permanece válida até que o objeto seja excluído.

A lista não requer nenhum suporte dos objetos que ele contém. Ele não realiza nenhum gerenciamento de armazenamento nem cópia nos objetos. Os objetos podem estar em várias listas.

Aproximadamente metade dos métodos nessa classe atuam em objetos únicos. Esses métodos têm o sufixo-I no nome do método. Os outros métodos agem em listas inteiras. Por exemplo, o método [**CBaseList:: AddAfter**](cbaselist-addafter.md) anexa uma lista a outra lista. Operações de objeto único retornam valores de posição ou **NULL** em caso de falha. As operações de lista retornarão **true** se for bem-sucedido ou **false** .



| Variáveis de membro protegido                             | Descrição                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [**contagem de m \_**](cbaselist-m-count.md)                  | Número de itens na lista.                                              |
| [**\_pFirst m**](cbaselist-m-pfirst.md)                | Ponteiro para o primeiro nó na lista.                                    |
| [**\_pLast m**](cbaselist-m-plast.md)                  | Ponteiro para o último nó na lista.                                     |
| Métodos Protegidos                                      | Descrição                                                               |
| [**Getpróximoi**](cbaselist-getnexti.md)                 | Recupera o item na posição especificada e avança a posição.  |
| [**GetI**](cbaselist-geti.md)                         | Recupera o item na posição especificada.                             |
| [**Localizar**](cbaselist-findi.md)                       | Recupera a primeira posição que contém o item especificado.               |
| [**RemoveHeadI**](cbaselist-removeheadi.md)           | Remove o primeiro item da lista.                                       |
| [**RemoveTailI**](cbaselist-removetaili.md)           | Remove o último item da lista.                                        |
| [**Mover para**](cbaselist-removei.md)                   | Remove o item na posição especificada.                               |
| [**Addcaudai**](cbaselist-addtaili.md)                 | Adiciona um item ao final da lista.                                      |
| [**Subtítuloi**](cbaselist-addheadi.md)                 | Adiciona um item à frente da lista.                                    |
| [**AddAfterI**](cbaselist-addafteri.md)               | Insere um item após a posição especificada.                             |
| [**Addantes de**](cbaselist-addbeforei.md)             | Insere um item antes da posição especificada.                            |
| Métodos públicos                                         | Descrição                                                               |
| [**CBaseList**](cbaselist-cbaselist.md)               | Método de construtor.                                                       |
| [**~ CBaseList**](cbaselist--cbaselist.md)            | Método destruidor.                                                        |
| [**RemoveAll**](cbaselist-removeall.md)               | Remove todos os nós da lista.                                          |
| [**GetHeadPositionI**](cbaselist-getheadpositioni.md) | Recupera a posição do primeiro item na lista.                     |
| [**GetTailPositionI**](cbaselist-gettailpositioni.md) | Recupera a posição do último item da lista.                      |
| [**Getcounteri**](cbaselist-getcounti.md)               | Recupera o número de itens na lista.                                |
| [**Avançar**](cbaselist-next.md)                         | Recupera a próxima posição na lista.                                  |
| [**/S**](cbaselist-prev.md)                         | Recupera a posição anterior na lista.                              |
| [**AddHead**](cbaselist-addhead.md)                   | Insere outra lista na frente desta lista.                           |
| [**Addcaudal**](cbaselist-addtail.md)                   | Acrescenta outra lista ao final desta lista.                             |
| [**AddAfter**](cbaselist-addafter.md)                 | Insere uma lista após a posição especificada.                              |
| [**Addantes**](cbaselist-addbefore.md)               | Insere uma lista antes da posição especificada.                             |
| [**MoveToTail**](cbaselist-movetotail.md)             | Divide a lista e acrescenta a parte de cabeçalho à cauda de outra lista. |
| [**MoveToHead**](cbaselist-movetohead.md)             | Divide a lista e insere a parte final no cabeçalho de outra lista. |
| [**Ordem**](cbaselist-reverse.md)                   | Inverte a ordem da lista.                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




