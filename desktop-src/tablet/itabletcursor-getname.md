---
description: Recupera o nome da caneta digitalizadora.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'Método ITabletCursor:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922647"
---
# <a name="itabletcursorgetname-method"></a>Método ITabletCursor:: GetName

Recupera o nome da caneta digitalizadora.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppwszName* \[ fora\]
</dt> <dd>

O nome da caneta digitalizadora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

