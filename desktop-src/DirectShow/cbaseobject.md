---
description: A classe CBaseObject é uma classe abstrata para implementar DirectShow objetos. Para implementar Component Object Model (COM), use a classe CUnknown, que deriva de CBaseObject.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Classe CBaseObject (Combase.h)
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
ms.openlocfilehash: 7809ec53746730f02f9b095ede3ae00b53f1fe55c21116c22d854c3d4b193e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910616"
---
# <a name="cbaseobject-class"></a>Classe CBaseObject

A **classe CBaseObject** é uma classe abstrata para implementar DirectShow objetos. Para implementar Component Object Model (COM), use a [**classe CUnknown,**](cunknown.md) que deriva de **CBaseObject**.



| Métodos de classe                                      | Descrição                            |
|----------------------------------------------------|----------------------------------------|
| [**Cbaseobject**](cbaseobject-cbaseobject.md)     | Método do construtor.                    |
| [**~CBaseObject**](cbaseobject--cbaseobject.md)   | Método destruidor.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Recupera a contagem de objetos ativos. |



 

## <a name="remarks"></a>Comentários

A maioria das classes DirectShow base derivam **de CBaseObject**. Essa classe fornece assistência de depuração mantendo uma contagem de todos os objetos DirectShow ativos durante o tempo de operação. A contagem de objetos é armazenada em uma variável de membro estática de classe:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



Em builds de depuração, a DLL declarará se ela for descarregada enquanto a contagem de objetos for maior que zero. Isso facilita o controle de vazamentos causados por problemas de contagem de referências.

O **construtor CBaseObject** recebe um argumento, um nome de depuração para o objeto . Esse nome é armazenado em uma tabela global na DLL. A [**função DbgDumpObjectRegister**](dbgdumpobjectregister.md) formatará uma lista dos objetos ativos na DLL e a enviará para a saída de depuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Base Classes](directshow-base-classes.md)
</dt> </dl>

 

 




