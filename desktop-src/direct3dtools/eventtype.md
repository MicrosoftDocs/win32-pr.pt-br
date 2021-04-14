---
description: Uma enumeração usada para indicar o tipo de um evento.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeração EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370168"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>Enumeração EVENTTYPE

Uma enumeração usada para indicar o tipo de um evento.

## <a name="syntax"></a>Syntax

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a>Constantes

<span id="ET_NONE"></span><span id="et_none"></span>**ET \_ nenhum**  
Um valor que corresponde a nenhum evento.

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_SESSIONSTART et**  
Um valor que corresponde a um evento de início de sessão.

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_SESSIONEND et**  
Um valor que corresponde a um evento de término de sessão.

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**\_PROCESSSTART et**  
Um valor que corresponde a um evento de início de processo.

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**\_PROCESSEND et**  
Um valor que corresponde a um evento Process end.

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_FRAMEBEGIN et**  
Um valor que corresponde a um evento de início de quadro.

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_FRAMEEND et**  
Um valor que corresponde a um evento de final de quadro. Não usado.

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**\_USEREVENTBEGIN et**  
Um valor que corresponde a um evento de início de evento do usuário.

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**\_USEREVENTEND et**  
Um valor que corresponde a um evento de término de evento do usuário. Não usado.

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_DEFAULTmarker et**  
Um valor que corresponde a um evento de marcador do usuário.

<span id="ET_CALL"></span><span id="et_call"></span>**\_chamada et**  
Um valor que corresponde a um evento de chamada.

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**objectcreation ET \_**  
Um valor que corresponde a um evento de criação de objeto.

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**ET \_ Population**  
Um valor que corresponde a um evento de população de objeto.

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**\_CALLSYNC et**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**\_desenho et**  
Um valor que corresponde a um evento de chamada de desenho.

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**\_expedição et**  
Um valor que corresponde a um evento de expedição.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>
