---
description: Recupera o objeto de botão especificado de uma caneta de tablet.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: Método ITabletCursor::GetButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938626"
---
# <a name="itabletcursorgetbutton-method"></a>Método ITabletCursor::GetButton

Recupera o objeto de botão especificado de uma caneta de tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iButton* \[ Em\]
</dt> <dd>

Identificador do botão a ser recuperado.

</dd> <dt>

*ppButton* \[ out\]
</dt> <dd>

O objeto de botão especificado pelo parâmetro *iButton.*

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

[**ITabletCursor Interface**](itabletcursor.md)
</dt> </dl>

 

 




