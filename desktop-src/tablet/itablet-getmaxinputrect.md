---
description: Recupera um retângulo que representa a área de entrada máxima do tablet.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: Método ITablet::GetMaxInputRect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 422c64a8f5f77b354f02ab9601f7a0c888669d61783afb636816efbdc2e13b27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883536"
---
# <a name="itabletgetmaxinputrect-method"></a>Método ITablet::GetMaxInputRect

Recupera um retângulo que representa a área de entrada máxima do tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Ponteiro para retângulo que representa a área de entrada máxima do tablet.

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

[**ITablet Interface**](itablet.md)
</dt> </dl>

 

 




