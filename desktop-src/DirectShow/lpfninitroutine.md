---
description: Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Ponteiro de função LPFNInitRoutine (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: c07f22b9dc261fe9d7b073a1f1ab93aa49e482fb70c53288aeaf606e6be9aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685076"
---
# <a name="lpfninitroutine-function-pointer"></a>Ponteiro de função LPFNInitRoutine

Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.

## <a name="syntax"></a>Sintaxe


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bLoading* 
</dt> <dd>

**True** quando a DLL for carregada, **false** quando a DLL for descarregada.

</dd> <dt>

*rclsid* 
</dt> <dd>

Ponteiro para o CLISD do objeto, especificado na variável de membro [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse ponteiro de função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




