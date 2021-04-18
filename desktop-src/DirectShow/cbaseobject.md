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
# <a name="cbaseobject-class"></a>Classe CBaseObject

A classe **CBaseObject** é uma classe abstrata para implementar objetos DirectShow. Para implementar objetos COM Component Object Model (COM), use a classe [**CUnknown**](cunknown.md) , que deriva de **CBaseObject**.



| Métodos de classe                                      | Descrição                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Método de construtor.                    |
| [**~ CBaseObject**](cbaseobject--cbaseobject.md)   | Método destruidor.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Recupera a contagem de objetos ativos. |



 

## <a name="remarks"></a>Comentários

A maioria das classes base do DirectShow deriva de **CBaseObject**. Essa classe fornece assistência de depuração mantendo uma contagem de todos os objetos do DirectShow ativos durante o tempo de execução. A contagem de objetos é armazenada em uma variável de membro de classe estática:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



Em compilações de depuração, a DLL será declarada se for descarregada enquanto a contagem de objetos for maior que zero. Isso torna mais fácil rastrear vazamentos causados por problemas de contagem de referência.

O construtor **CBaseObject** Obtém um argumento, um nome de depuração para o objeto. Esse nome é armazenado em uma tabela global na DLL. A função [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) formata uma lista dos objetos ativos na dll e a envia para a saída de depuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes base do DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




