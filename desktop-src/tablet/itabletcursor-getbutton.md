---
description: Recupera o objeto de botão especificado de uma caneta digitalizadora.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Método ITabletCursor:: getbutton'
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
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762151"
---
# <a name="itabletcursorgetbutton-method"></a>Método ITabletCursor:: getbutton

Recupera o objeto de botão especificado de uma caneta digitalizadora.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iButton* \[ no\]
</dt> <dd>

Identificador do botão a ser recuperado.

</dd> <dt>

*ppButton* \[ fora\]
</dt> <dd>

O objeto Button especificado pelo parâmetro *iButton* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




