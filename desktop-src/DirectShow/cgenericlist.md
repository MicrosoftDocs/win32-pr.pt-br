---
description: O modelo de classe CGenericList que implementa uma lista específica de tipo. Para obter mais informações, consulte CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Classe CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752289"
---
# <a name="cgenericlist-class"></a>Classe CGenericList

![hierarquia de classe CGenericList](images/list01.png)

O `CGenericList` modelo de classe que implementa uma lista específica de tipo. Para obter mais informações, consulte [**CBaseList**](cbaselist.md).

Para usar este modelo, declare uma variável do tipo `CGenericList` com um argumento de modelo que define o tipo de objeto na lista. Por exemplo, a instrução a seguir declara uma lista de objetos [**CBaseFilter**](cbasefilter.md) :


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



Para sua conveniência, Wxlist. h define os seguintes tipos de lista:

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| Métodos públicos                                          | Descrição                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**CGenericList**](cgenericlist-cgenericlist.md)       | Método de construtor.                                                      |
| [**~ CGenericList**](cgenericlist--cgenericlist.md)     | Método destruidor.                                                       |
| [**GetHeadPosition**](cgenericlist-getheadposition.md) | Recupera a posição do primeiro item na lista.                    |
| [**GetTailPosition**](cgenericlist-gettailposition.md) | Recupera a posição do último item da lista.                     |
| [**GetCount**](cgenericlist-getcount.md)               | Recupera o número de itens na lista.                               |
| [**GetNext**](cgenericlist-getnext.md)                 | Recupera o item na posição especificada e avança a posição. |
| [**Obter**](cgenericlist-get.md)                         | Recupera o item na posição especificada.                            |
| [**GetHead**](cgenericlist-gethead.md)                 | Recupera o item no cabeçalho da lista.                              |
| [**RemoveHead**](cgenericlist-removehead.md)           | Remove o primeiro item da lista.                                      |
| [**RemoveTail**](cgenericlist-removetail.md)           | Remove o último item da lista.                                       |
| [**Remover**](cgenericlist-remove.md)                   | Remove o item na posição especificada.                              |
| [**Addantes**](cgenericlist-addbefore.md)             | Insere um item ou uma lista antes da posição especificada.                   |
| [**AddAfter**](cgenericlist-addafter.md)               | Insere um item ou uma lista após a posição especificada.                    |
| [**AddHead**](cgenericlist-addhead.md)                 | Adiciona um item ou lista à frente da lista.                           |
| [**Addcaudal**](cgenericlist-addtail.md)                 | Anexa um item ou uma lista ao final da lista.                          |
| [**Localizar**](cgenericlist-find.md)                       | Recupera a primeira posição que contém o item especificado.              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxlist. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




