---
description: Retorna o número de objetos de cursor associados ao Tablet.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Método ITablet:: GetCursorCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 02ad52e5ad75d4c71129ec7987347121c6152c01071e797c7b169327fdeb3614
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883856"
---
# <a name="itabletgetcursorcount-method"></a>Método ITablet:: GetCursorCount

Retorna o número de objetos de cursor associados ao Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcCurs* \[ fora\]
</dt> <dd>

O número de objetos de cursor associados ao Tablet.

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

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




