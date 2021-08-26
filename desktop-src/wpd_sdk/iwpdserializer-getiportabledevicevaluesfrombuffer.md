---
description: O método GetIPortableDeviceValuesFromBuffer deserializa uma matriz de byte para uma interface IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: Método IWpdSerializer::GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes.h)
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
ms.openlocfilehash: ac33bf0cfb04363d40e4efeff13db1cb2504ce2dcb7ece4d9b10ac3d08dff83f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054956"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Método IWpdSerializer::GetIPortableDeviceValuesFromBuffer

O **método GetIPortableDeviceValuesFromBuffer** deserializa uma matriz de byte para uma interface **IPortableDeviceValues.**

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

*pBuffer* \[ Em\]
</dt> <dd>

Ponteiro para o buffer a ser desterlizado.

</dd> <dt>

*dwInputBufferLength* \[ Em\]
</dt> <dd>

**DWORD** que especifica o tamanho do buffer, em bytes.

</dd> <dt>

*ppParams* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) criada a partir do buffer. O aplicativo é responsável por chamar **Release** na interface .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Um argumento de ponteiro necessário era **NULL.**<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Ocorreu um erro de conversão não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWpdSerializer Interface**](iwpdserializer.md)
</dt> </dl>

 

 




