---
description: O objeto Wia é o ponto de entrada para todas as Windows de script WIA (Aquisição de Imagem).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objeto Wia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 38dc5f7ac4440320827e009a7fd38dd6554ceb70
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469613"
---
# <a name="wia-object"></a>Objeto Wia

O **objeto Wia** é o ponto de entrada para todas as Windows de script WIA (Aquisição de Imagem). Qualquer aplicativo que usa o modelo de script WIA deve criar [**um objeto SafeWia**](-wia-safewia.md) ou **Wia.** Use esse objeto para enumerar e criar dispositivos e receber notificação de eventos de hardware.

> [!Note]  
> Esse objeto não é seguro para scripts. Para uma versão desse objeto que é segura para scripts, consulte [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Membros

O **objeto Wia** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O **objeto Wia** tem esses eventos.



| Evento                                                                 | Descrição                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento que ocorre quando um novo dispositivo de hardware WIA está conectado.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento que ocorre quando um novo dispositivo de hardware WIA é desconectado.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento que ocorre quando uma transferência de dados é concluída com êxito.<br/> |



 

### <a name="methods"></a>Métodos

O **objeto Wia** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criar**](-wia-iwia-create.md) | O [**método**](-wia-iwia-create.md) Create do **objeto Wia** faz uma conexão com o dispositivo WIA especificado e retorna um [**objeto Item**](-wia-item.md) que representa o dispositivo.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto Wia** tem essas propriedades.




| Propriedade | Tipo de acesso | Descrição | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br /> | Somente leitura<br /> | Coleção de <a href="-wia-deviceinfo.md"><strong>objetos DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador. Somente leitura. <br /><blockquote>[!Note]<br />Essa coleção é baseada em 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4.90 ou posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ Wia<br/>                                                                                         |



 

 




