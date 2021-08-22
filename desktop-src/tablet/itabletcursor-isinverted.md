---
description: Indica se a caneta está de cabeça para baixo.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Método ITabletCursor:: inverted'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 81bbb5f4f93026e0d6910cb7f23d0a7d2ddeea5595e87f816faa016d22986d0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223062"
---
# <a name="itabletcursorisinverted-method"></a>Método ITabletCursor:: inverted

Indica se a caneta está de cabeça para baixo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                             | Descrição                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | A caneta é invertida.<br/>        |
| <dl> <dt>**\_falso**</dt> </dl> | A caneta não está invertida.<br/>    |
| <dl> <dt>**E \_ falha**</dt> </dl>  | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

 




