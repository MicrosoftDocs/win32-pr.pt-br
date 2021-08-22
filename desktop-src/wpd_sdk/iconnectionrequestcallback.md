---
description: Define um único método de retorno de chamada.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interface IConnectionRequestCallback (Devpkey.h)
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
ms.openlocfilehash: 53e1549767c8577507b3126b3a293dfe4e523612809c144ff24c04dce4ab1ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697414"
---
# <a name="iconnectionrequestcallback-interface"></a>Interface IConnectionRequestCallback

A interface **IConnectionRequestCallback** define um único método de retorno de chamada. Um Windows wpd (dispositivos portáteis) implementa essa interface opcional Component Object Model (COM) para receber notificações sobre solicitações concluídas e cancelar solicitações pendentes. As solicitações são enviadas usando os métodos [**IPortableDeviceConnector::Conexão**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) [**e IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="members"></a>Membros

A interface **IConnectionRequestCallback** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionRequestCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IConnectionRequestCallback** tem esses métodos.



| Método                                                      | Descrição                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Oncomplete**](iconnectionrequestcallback-oncomplete.md) | Notifica um aplicativo de que uma solicitação agendada anteriormente foi concluída.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

