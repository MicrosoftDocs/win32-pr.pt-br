---
title: Método GetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Um método genérico para obter propriedades de trabalho da otimização de entrega (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Método GetProperty
- Método GetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918538"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>Método IBackgroundCopyJob5:: GetProperty

Um método genérico para obter propriedades de trabalho da otimização de entrega (DO).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyId* \[ no\]
</dt> <dd>

A ID da propriedade que está sendo obtida especificada como um [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valor de enumeração.

</dd> <dt>

*pPropertyValue* \[ fora\]
</dt> <dd>

O valor da propriedade retornado como uma União de BITS_JOB_PROPERTY_VALUE.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna os valores de retorno a seguir.



| Código de retorno                                                                          | Descrição        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Sucesso<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





