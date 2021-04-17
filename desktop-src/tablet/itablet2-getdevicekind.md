---
description: Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Método ITablet2:: GetDeviceKind'
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
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772723"
---
# <a name="itablet2getdevicekind-method"></a>Método ITablet2:: GetDeviceKind

Retorna o tipo de dispositivo de hardware que o objeto do Tablet representa, como mouse, caneta ou toque.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pKind* \[ fora\]
</dt> <dd>

Valor de enumeração que indica o tipo de Tablet, como mouse, caneta ou toque.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface e o método foram introduzidos no Windows Vista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITablet2**](itablet2.md)
</dt> <dt>

[**Enumeração de tipo de \_ dispositivo tablet \_**](tablet-device-kind.md)
</dt> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




