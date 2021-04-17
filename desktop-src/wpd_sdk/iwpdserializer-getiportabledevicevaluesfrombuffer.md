---
description: O método GetIPortableDeviceValuesFromBuffer desserializa uma matriz de bytes para uma interface IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Método IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787551"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Método IWpdSerializer:: GetIPortableDeviceValuesFromBuffer

O método **GetIPortableDeviceValuesFromBuffer** desserializa uma matriz de bytes para uma interface **IPortableDeviceValues** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBuffer* \[ no\]
</dt> <dd>

Ponteiro para o buffer a ser desserializado.

</dd> <dt>

*dwInputBufferLength* \[ no\]
</dt> <dd>

**DWORD** que especifica o tamanho do buffer, em bytes.

</dd> <dt>

*ppParams* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) criada a partir do buffer. O aplicativo é responsável por chamar o **lançamento** na interface.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um argumento de ponteiro necessário era **nulo**.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Ocorreu um erro de conversão não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




