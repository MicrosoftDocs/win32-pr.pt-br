---
description: O NLA é capaz de fornecer aos clientes a notificação de alterações de local de rede. O mecanismo usado para solicitar a notificação de eventos de alteração é uma combinação das funções WSALookupServiceBegin, WSANSPIoctl e WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notificação do NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8e7309fe6845d822702ffd81448999e2472ebdd37a6949812f622110ee9d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822661"
---
# <a name="notification-from-nla"></a>Notificação do NLA

O NLA é capaz de fornecer aos clientes a notificação de alterações de local de rede. O mecanismo usado para solicitar a notificação de eventos de alteração é uma combinação das funções [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)e [**WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

Para receber uma notificação de alteração do NLA, um cliente deve primeiro chamar o [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) para obter um manipular de procura NLA SP válido. Em seguida, o cliente pode [**chamar WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) ou [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) em qualquer ordem; para se registrar para notificação, chame a **função WSANSPIoctl** com o código de controle SIO NSP NOTIFY CHANGE definido no parâmetro \_ \_ \_ *dwControlCode.*

A [**função WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retorna WSA \_ E NO MORE como um \_ \_ delimiter definido. Quando um cliente é registrado para notificação usando a função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) e **WSALookupServiceNext** retorna WSA E NO MORE, chamar \_ \_ \_ **WSALookupServiceNext** novamente revela se ocorreu uma alteração:

-   Se nenhuma alteração tiver ocorrido desde o WSA \_ E \_ NO MORE \_ anterior, o WSA \_ E NO MORE será \_ \_ retornado.
-   Se uma alteração tiver ocorrido ou se uma alteração tiver ocorrido e uma chamada de sondagem for feita, a chamada de função [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) retornará redes como estruturas [**WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) com um dos seguintes sinalizadores definidos em seu membro **dwOutputFlags:**

    <dl> O \_ RESULTADO É \_ ADICIONADO  
    O RESULTADO \_ É \_ ALTERADO  
    O \_ RESULTADO \_ É EXCLUÍDO  
    </dl>

A notificação de alteração é fornecida para todos os campos que foram alterados desde que o alçamento de pesquisa NLA foi obtido com a chamada de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ou desde a última enumeração que resultou no erro WSA \_ E NO \_ \_ MORE. Quando todas as informações de local de rede alteradas são fornecidas, o WSA \_ E NO MORE é \_ \_ retornado. Os clientes podem emita uma chamada de função [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) no mesmo alça de consulta a qualquer momento, uma de cada vez, com o sinalizador SIO \_ NSP \_ NOTIFY CHANGE \_ definido. Essa funcionalidade permite que um cliente recicle o controle de consulta continuamente, aliviando assim o cliente de ter que manter as informações de estado de alteração por conta própria. Depois que um cliente não precisar mais de notificações de alteração, ele deverá fechar o alçamento de consulta usando a [**função WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

 

 



