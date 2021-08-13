---
description: Retorna o tipo de dispositivo de hardware que o objeto de tablet representa, como mouse, caneta ou toque.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: Método ITablet2::GetDeviceKind
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450523"
---
# <a name="itablet2getdevicekind-method"></a>Método ITablet2::GetDeviceKind

Retorna o tipo de dispositivo de hardware que o objeto de tablet representa, como mouse, caneta ou toque.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pKind* \[ out\]
</dt> <dd>

Valor de enumeração que indica o tipo de tablet, como mouse, caneta ou toque.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface e método foram introduzidos no Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITablet2 Interface**](itablet2.md)
</dt> <dt>

[**\_Enumeração TIPO \_ DE DISPOSITIVO TABLET**](tablet-device-kind.md)
</dt> <dt>

[**ITablet Interface**](itablet.md)
</dt> </dl>

 

 




