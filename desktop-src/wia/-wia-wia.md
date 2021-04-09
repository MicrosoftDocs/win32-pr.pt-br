---
description: O objeto WIA é o ponto de entrada para toda a funcionalidade de script da aquisição de imagem do Windows (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Objeto WIA
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
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090486"
---
# <a name="wia-object"></a>Objeto WIA

O objeto **WIA** é o ponto de entrada para toda a funcionalidade de script da aquisição de imagem do Windows (WIA). Qualquer aplicativo que usa o modelo de script WIA deve criar um objeto [**SafeWia**](-wia-safewia.md) ou **WIA** . Use esse objeto para enumerar e criar dispositivos e para receber notificações de eventos de hardware.

> [!Note]  
> Este objeto não é seguro para scripts. Para obter uma versão desse objeto que seja segura para scripts, consulte [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Membros

O objeto **WIA** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O objeto **WIA** tem esses eventos.



| Evento                                                                 | Descrição                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento que ocorre quando um novo dispositivo de hardware WIA é conectado.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento que ocorre quando um novo dispositivo de hardware WIA é desconectado.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento que ocorre quando uma transferência de dados é concluída com êxito.<br/> |



 

### <a name="methods"></a>Métodos

O objeto **WIA** tem esses métodos.



| Método                             | Descrição                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criada**](-wia-iwia-create.md) | O método [**Create**](-wia-iwia-create.md) do objeto **WIA** faz uma conexão com o dispositivo WIA especificado e retorna um objeto [**Item**](-wia-item.md) que representa o dispositivo.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **WIA** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br/></td>
<td style="text-align: left;">Somente leitura<br/></td>
<td style="text-align: left;">Coleção de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos os dispositivos instalados no computador. Somente leitura. <br/>
<blockquote>
[!Note]<br />
Esta coleção é baseada em 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versão 4,90 ou posterior)</dt> </dl> |
| IID<br/>                      | CLSID \_ WIA<br/>                                                                                         |



 

 




