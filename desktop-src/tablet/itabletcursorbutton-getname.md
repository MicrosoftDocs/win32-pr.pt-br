---
description: Recupera o nome do botão da caneta.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Método ITabletCursorButton:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811085"
---
# <a name="itabletcursorbuttongetname-method"></a>Método ITabletCursorButton:: GetName

Recupera o nome do botão da caneta.

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

O nome do botão da caneta.

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

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

