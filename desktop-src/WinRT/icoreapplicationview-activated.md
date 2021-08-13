---
description: ocorre quando um aplicativo da Windows Store é ativado.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Evento ICoreApplicationView:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560990"
---
# <a name="icoreapplicationviewactivated-event"></a>Evento ICoreApplicationView:: Activated

ocorre quando um aplicativo da Windows Store é ativado.

## <a name="syntax"></a>Sintaxe


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*manipulador* \[ no\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Não chame o método [**Exit**](/previous-versions//hh438368(v=vs.85)) de dentro do *manipulador*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                               |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
