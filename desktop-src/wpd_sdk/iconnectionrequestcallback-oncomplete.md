---
description: Notifica um aplicativo de que uma solicitação de conexão ou desconexão agendada anteriormente para o dispositivo MTP/Bluetooth foi concluída.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'Método IConnectionRequestCallback:: OnComplete (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829091"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Método IConnectionRequestCallback:: OnComplete

O método **OnComplete** notifica um aplicativo de que uma solicitação de conexão ou desconexão agendada anteriormente para o dispositivo MTP/Bluetooth foi concluída

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hrStatus* \[ no\]
</dt> <dd>

O status da solicitação para conectar ou desconectar um determinado dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo implementa a interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para receber notificações sobre solicitações concluídas e para cancelar solicitações pendentes.

Os dispositivos portáteis do Windows (WPD) chamam esse método para notificar um aplicativo de que uma solicitação agendada anteriormente foi concluída. Cada solicitação pode ser rastreada e cancelada por seu retorno de chamada fornecido pelo aplicativo. Portanto, se o aplicativo precisar enviar várias solicitações ao mesmo tempo usando o mesmo objeto [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , cada solicitação deverá passar um objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) exclusivo como o parâmetro de entrada para os métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| parâmetro<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




