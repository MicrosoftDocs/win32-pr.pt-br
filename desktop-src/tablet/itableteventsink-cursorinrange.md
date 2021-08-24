---
description: Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Método ITabletEventSink:: CursorInRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c9878b4c3cd28727c5d54e59a52f3fe85a44832203f70b6ff042c6beeb579dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883476"
---
# <a name="itableteventsinkcursorinrange-method"></a>Método ITabletEventSink:: CursorInRange

Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TCID* \[ no\]
</dt> <dd>

O identificador do objeto do Tablet que detectou a caneta.

</dd> <dt>

*CID* 
</dt> <dd>

O identificador do objeto de caneta que vem no intervalo do digitalizador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




