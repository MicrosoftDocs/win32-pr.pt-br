---
description: As \_ constantes TAPIERR fornecem informações relacionadas a falhas de execução de função.
ms.assetid: 6d1cf18b-efeb-4703-9b8e-fce59b61b63f
title: Constantes de TAPIERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e8a60e2a625ff456a4a8aa2730b80000e92ff54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755170"
---
# <a name="tapierr_-constants"></a>\_Constantes TAPIERR

As **\_ constantes TAPIERR** fornecem informações relacionadas a falhas de execução de função.

<dl> <dt>

<span id="TAPIERR_CONNECTED"></span><span id="tapierr_connected"></span>**TAPIERR \_ conectado**
</dt> <dd> <dl> <dt>



A operação não pode ser executada enquanto o estado de chamada está conectado.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTBUSY"></span><span id="tapierr_destbusy"></span>**TAPIERR \_ DESTBUSY**
</dt> <dd> <dl> <dt>



O destino da chamada está ocupado.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTNOANSWER"></span><span id="tapierr_destnoanswer"></span>**TAPIERR \_ DESTNOANSWER**
</dt> <dd> <dl> <dt>



O destino da chamada não respondeu.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTUNAVAIL"></span><span id="tapierr_destunavail"></span>**TAPIERR \_ DESTUNAVAIL**
</dt> <dd> <dl> <dt>



O destino da chamada não está disponível.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICECLASSUNAVAIL"></span><span id="tapierr_deviceclassunavail"></span>**TAPIERR \_ DEVICECLASSUNAVAIL**
</dt> <dd> <dl> <dt>



A classe de dispositivo necessária não está disponível.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEIDUNAVAIL"></span><span id="tapierr_deviceidunavail"></span>**TAPIERR \_ DEVICEIDUNAVAIL**
</dt> <dd> <dl> <dt>



O identificador de dispositivo necessário não está disponível.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEINUSE"></span><span id="tapierr_deviceinuse"></span>**TAPIERR \_ DEVICEINUSE**
</dt> <dd> <dl> <dt>



O dispositivo necessário está em uso.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DROPPED"></span><span id="tapierr_dropped"></span>**TAPIERR \_ removido**
</dt> <dd> <dl> <dt>



A chamada foi descartada.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDESTADDRESS"></span><span id="tapierr_invaldestaddress"></span>**TAPIERR \_ INVALDESTADDRESS**
</dt> <dd> <dl> <dt>



O ponteiro para o endereço de destino não é válido, é **nulo** ou a cadeia de caracteres de endereço de destino é muito longa.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICECLASS"></span><span id="tapierr_invaldeviceclass"></span>**TAPIERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



A classe de dispositivo solicitada não é válida.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICEID"></span><span id="tapierr_invaldeviceid"></span>**TAPIERR \_ INVALDEVICEID**
</dt> <dd> <dl> <dt>



O identificador de classe de dispositivo solicitado não é válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALPOINTER"></span><span id="tapierr_invalpointer"></span>**TAPIERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



O ponteiro não faz referência a um local de memória válido. Um ou mais dos ponteiros *lpszDestAddress*, *lpszAppName*, *lpszCalledParty* ou *lpszComment* foram especificados, mas são inválidos.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALWINDOWHANDLE"></span><span id="tapierr_invalwindowhandle"></span>**TAPIERR \_ INVALWINDOWHANDLE**
</dt> <dd> <dl> <dt>



O identificador de janela não é válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOREQUESTRECIPIENT"></span><span id="tapierr_norequestrecipient"></span>**TAPIERR \_ NOREQUESTRECIPIENT**
</dt> <dd> <dl> <dt>



Nenhum aplicativo de destinatário está disponível para lidar com a solicitação. O usuário deve iniciar o aplicativo de destinatário e tentar novamente.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOTADMIN"></span><span id="tapierr_notadmin"></span>**TAPIERR não \_ admin**
</dt> <dd> <dl> <dt>



A operação solicitada requer privilégios de administrador.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTCANCELLED"></span><span id="tapierr_requestcancelled"></span>**TAPIERR \_ REQUESTCANCELLED**
</dt> <dd> <dl> <dt>



A solicitação de telefonia assistida foi cancelada.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTFAILED"></span><span id="tapierr_requestfailed"></span>**TAPIERR \_ REQUESTFAILED**
</dt> <dd> <dl> <dt>



A solicitação falhou por motivos não especificados.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTQUEUEFULL"></span><span id="tapierr_requestqueuefull"></span>**TAPIERR \_ REQUESTQUEUEFULL**
</dt> <dd> <dl> <dt>



Um aplicativo de destinatário está ativo, mas a fila de solicitação está cheia ou não há memória suficiente para expandir a fila. O aplicativo pode tentar novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNREQUESTID"></span><span id="tapierr_unknownrequestid"></span>**TAPIERR \_ UNKNOWNREQUESTID**
</dt> <dd> <dl> <dt>



O identificador de solicitação referenciado não é válido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNWINHANDLE"></span><span id="tapierr_unknownwinhandle"></span>**TAPIERR \_ UNKNOWNWINHANDLE**
</dt> <dd> <dl> <dt>



Um identificador de janela desconhecido foi referenciado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Quaisquer outros valores de TAPIERR \_ são obsoletos e não devem ser usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




