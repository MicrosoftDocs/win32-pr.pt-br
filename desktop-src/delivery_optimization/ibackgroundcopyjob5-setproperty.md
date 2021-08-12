---
title: Método SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Um método genérico para definir propriedades de trabalho de otimização de entrega (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- Método SetProperty
- Método SetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f9b7dab17780572a59e12dde9905c3d8db23895e6564aac47cb6eb2d984bfaf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542679"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>Método IBackgroundCopyJob5:: SetProperty

Um método genérico para definir propriedades de trabalho de otimização de entrega (DO).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyId* \[ no\]
</dt> <dd>

A ID da propriedade que está sendo definida como um [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valor de enumeração.

</dd> <dt>

*PropertyValue* \[ no\]
</dt> <dd>

O valor da propriedade que está sendo definida. Para manter um valor cujo tipo é apropriado para a propriedade, esse valor é especificado por meio da União de [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) que é composta por todos os tipos de propriedade conhecidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna os valores de retorno a seguir.



| Código de retorno                                                                          | Descrição        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Êxito<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





