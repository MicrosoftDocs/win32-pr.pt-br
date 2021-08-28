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
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619566"
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

## <a name="return-value"></a>Valor retornado

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

 

 





