---
description: Define um único método de retorno de chamada.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interface IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922829"
---
# <a name="iconnectionrequestcallback-interface"></a>Interface IConnectionRequestCallback

A interface **IConnectionRequestCallback** define um único método de retorno de chamada. Um aplicativo de dispositivos portáteis do Windows (WPD) implementa essa interface opcional de Component Object Model (COM) para receber notificações sobre solicitações concluídas e para cancelar solicitações pendentes. As solicitações são enviadas usando os métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) e [**IPortableDeviceConnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="members"></a>Membros

A interface **IConnectionRequestCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionRequestCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IConnectionRequestCallback** tem esses métodos.



| Método                                                      | Descrição                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Por completo**](iconnectionrequestcallback-oncomplete.md) | Notifica um aplicativo de que uma solicitação agendada anteriormente foi concluída.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| parâmetro<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

