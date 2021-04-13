---
description: O NLA é capaz de fornecer aos clientes notificação de alterações de local de rede. O mecanismo usado para solicitar a notificação de eventos de alteração é uma combinação das funções WSALookupServiceBegin, WSANSPIoctl e WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notificação do NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501680"
---
# <a name="notification-from-nla"></a>Notificação do NLA

O NLA é capaz de fornecer aos clientes notificação de alterações de local de rede. O mecanismo usado para solicitar a notificação de eventos de alteração é uma combinação das funções [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)e [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

Para receber notificação de alteração da NLA, um cliente deve primeiro chamar o [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para obter um identificador de pesquisa do NLA SP válido. Em seguida, o cliente pode chamar [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) ou [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) em qualquer ordem; para se registrar para notificação, chame a função **WSANSPIoctl** com o \_ código de controle de alteração sio NSP \_ notificar \_ definido no parâmetro *dwControlCode* .

A função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retorna WSA \_ E \_ não \_ mais como um delimitador de conjunto. Quando um cliente tiver se registrado para notificação usando a função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) e **WSALOOKUPSERVICENEXT** retornar o WSA \_ e \_ não \_ mais, chamar **WSALookupServiceNext** novamente revela se uma alteração ocorreu:

-   Se nenhuma alteração ocorreu desde o WSA \_ e \_ não mais anterior \_ , o WSA \_ e \_ não \_ mais será retornado.
-   Se uma alteração tiver ocorrido ou se uma alteração tiver ocorrido e uma chamada de sondagem for feita, a chamada de função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retornará redes como estruturas [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , com um dos seguintes sinalizadores definidos em seu membro **dwOutputFlags** :

    <dl> o resultado \_ é \_ adicionado  
    o resultado \_ é \_ alterado  
    o resultado \_ é \_ excluído  
    </dl>

A notificação de alteração é fornecida para todos os campos que foram alterados desde que o identificador de pesquisa NLA foi obtido com a chamada de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) , ou desde a última enumeração que resultou no \_ erro WSA E \_ não \_ mais. Quando todas as informações de local de rede alteradas são fornecidas, o WSA \_ E \_ não \_ mais é retornado. Os clientes podem reemitir uma chamada de função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) no mesmo identificador de consulta a qualquer momento, uma de cada vez, com o \_ sinalizador de alteração sio NSP \_ notificar \_ . Esse recurso permite que um cliente recicle o identificador de consulta em uma base contínua, aliviando, assim, que o cliente precise manter informações de estado de alteração por conta própria. Quando um cliente não precisar mais de notificações de alteração, ele deverá fechar o identificador de consulta usando a função [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

 

 



