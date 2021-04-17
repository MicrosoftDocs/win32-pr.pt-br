---
description: O método GetIPortableDeviceKeyCollectionValue recupera um valor de IPortableDeviceKeyCollection (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Método IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759578"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>Método IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue

O método **GetIPortableDeviceKeyCollectionValue** recupera um valor de **IPORTABLEDEVICEKEYCOLLECTION** (tipo VT \_ desconhecido) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.

</dd> <dt>

*ppValue* \[ fora\]
</dt> <dd>

Ponteiro para o ponteiro de interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperado. O chamador é responsável por chamar **Release** na interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada por *chave* não é uma interface **IPortableDeviceKeyCollection** .<br/> |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>                             |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> </dl>

 

 




