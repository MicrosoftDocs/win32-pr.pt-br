---
description: Notifica um aplicativo de que uma solicitação Conexão agendada anteriormente ou Desconectar para o dispositivo MTP/Bluetooth foi concluída.
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: Método IConnectionRequestCallback::OnComplete (Devpkey.h)
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
ms.openlocfilehash: b21248cde95d4b58accb7e629efedfc7c05eef7b08f411e240314a6a07690b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843184"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a>Método IConnectionRequestCallback::OnComplete

O **método OnComplete** notifica um aplicativo de que uma solicitação Conexão agendada anteriormente ou Desconectar para o dispositivo MTP/Bluetooth foi concluída

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hrStatus* \[ Em\]
</dt> <dd>

O status da solicitação para se conectar ou desconectar um determinado dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo implementa a interface [**IConnectionRequestCallback**](iconnectionrequestcallback.md) para receber notificações sobre solicitações concluídas e cancelar solicitações pendentes.

Windows O WPD (Dispositivos Portáteis) chama esse método para notificar um aplicativo de que uma solicitação agendada anteriormente foi concluída. Cada solicitação pode ser rastreada e cancelada por seu retorno de chamada fornecido pelo aplicativo. Portanto, se o aplicativo precisar enviar várias solicitações ao mesmo tempo usando o mesmo objeto [**IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) cada solicitação deverá ser passada um objeto [**IConnectionRequestCallback**](iconnectionrequestcallback.md) exclusivo como o parâmetro de entrada para os métodos [**IPortableDeviceConnector::Conexão**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionRequestCallback**](iconnectionrequestcallback.md)
</dt> </dl>

 

 




