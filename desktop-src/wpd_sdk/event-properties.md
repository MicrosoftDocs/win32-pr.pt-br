---
description: Windows Os dispositivos portáteis oferecem suporte às seguintes propriedades de evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propriedades do evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f5220b7cd3b0acfb70788a62138a7da3a4ebac008a51e90bbc93308ae2624300
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055346"
---
# <a name="event-properties"></a>Propriedades do evento

Windows Os dispositivos portáteis oferecem suporte às seguintes propriedades de evento.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>VarType</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Reservado para uso futuro.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Um valor booliano que especifica se o evento é difundido para todos os clientes. Os clientes podem receber esse evento registrando seu retorno de chamada com <strong>IPortableDevice:: Advise</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Um valor booliano que especifica se a hierarquia filho do objeto foi alterada. Esse parâmetro é usado para notificar o chamador de que alguns filhos do objeto especificado foram adicionados ou removidos. Normalmente, a alteração da hierarquia é iniciada no lado do dispositivo. Os clientes podem precisar enumerar novamente os filhos dessa pasta para manter suas exibições atualizadas.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Um valor que identifica um evento.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>O cookie é devolvido a um cliente quando ele solicita uma criação de objeto chamando o método <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent:: CreateObjectWithPropertiesAndData</strong></a> . Esse parâmetro é adicionado como uma conveniência para ajudar o chamador a ligar um evento de objeto adicionado à solicitação enviada para criar o objeto. O driver passa esse cookie de volta como o <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> valor de retorno ao processar o comando <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Um valor que identifica exclusivamente o objeto pai. Essa propriedade é semelhante a <strong>WPD_OBJECT_PARENT_ID</strong>, mas essa ID não é alterada entre sessões.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Um valor que especifica o progresso de uma operação em execução no momento. O valor dessa propriedade pode variar de 0 a 100, com 100 indicando que a operação foi concluída.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Um valor que indica o estado atual da operação, por exemplo, iniciado, em execução, parado e assim por diante. Os valores possíveis desse parâmetro são da enumeração <strong>WPD_OPERATION_STATES</strong> definida em PortableDevice. h. Os valores possíveis são:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Um valor que especifica o dispositivo que originou o evento. Esse é o identificador de dispositivo ou serviço fornecido pelo sistema de plug-and-Play (PnP) e é a mesma cadeia de caracteres usada nos métodos <strong>IPortableDevice:: Open</strong>ou <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService:: Open</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Uma cadeia de caracteres que é usada por um driver WPD para identificar a operação de um método de serviço de dispositivo. Os aplicativos não devem usar esse parâmetro diretamente.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




