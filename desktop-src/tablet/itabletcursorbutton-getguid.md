---
description: Recupera o identificador exclusivo do botão de caneta.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: Método ITabletCursorButton::GetGuid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f4492aa98630491730435080981172bc60a1eeccfe0c84ed76e3b4d504a79ad1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844276"
---
# <a name="itabletcursorbuttongetguid-method"></a>Método ITabletCursorButton::GetGuid

Recupera o identificador exclusivo do botão de caneta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguidBtn* \[ out\]
</dt> <dd>

Um valor exclusivo que identifica o botão de caneta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletCursorButton Interface**](itabletcursorbutton.md)
</dt> </dl>

 

 




