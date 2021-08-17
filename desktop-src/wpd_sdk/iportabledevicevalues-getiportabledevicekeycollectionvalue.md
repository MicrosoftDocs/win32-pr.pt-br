---
description: O método GetIPortableDeviceKeyCollectionValue recupera um valor IPortableDeviceKeyCollection (tipo VT UNKNOWN) especificado \_ por uma chave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: Método IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 13a7ccde6a7cf5a73c78cc382341f7d750d9032cbfd8d69bdcfd3e318eeccece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194097"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>Método IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue

O **método GetIPortableDeviceKeyCollectionValue** recupera um valor **IPortableDeviceKeyCollection** (tipo VT UNKNOWN) especificado \_ por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ Em\]
</dt> <dd>

Uma **chave REFPROPERTYKEY** que especifica o item a ser recuperado.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Ponteiro para o ponteiro da interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperado. O chamador é responsável por chamar **Release** na interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada pela *chave não* é uma interface **IPortableDeviceKeyCollection.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>                             |



 

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar esse método, consulte Recuperando eventos [de serviço com suporte.](retrieving-supported-events.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> </dl>

 

 




