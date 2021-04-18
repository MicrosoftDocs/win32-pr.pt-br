---
title: Método IWMDRMDevice SetMeterResponse
description: O método SetMeterResponse define a resposta de medição.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Método SetMeterResponse Windows Media Gerenciador de Dispositivos
- Método SetMeterResponse Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810598"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>Método IWMDRMDevice:: SetMeterResponse

O método **SetMeterResponse** define a resposta de medição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbMeterResponse* \[ no\]
</dt> <dd>

A resposta de medição a ser definida.

</dd> <dt>

*cbMeterResponse* \[ no\]
</dt> <dd>

Tamanho da resposta de medição, em bytes.

</dd> <dt>

*pdwFlags* \[ fora\]
</dt> <dd>

Sinalizadores de resposta. Esse valor deve ser um dos sinalizadores a seguir.



| Sinalizador                            | Descrição              |
|---------------------------------|--------------------------|
| \_ \_ todas as respostas de medidor de WMDRM \_     | Todas as respostas do medidor.     |
| \_parcial de \_ resposta de medidor de WMDRM \_ | Respostas de medidor parciais. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





