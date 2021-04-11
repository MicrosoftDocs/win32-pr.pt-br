---
title: Inicialização do ponto de acesso do EAP
description: Na inicialização, o AP (ponto de acesso) consulta o registro em busca de protocolos de autenticação instalados.
ms.assetid: e230e01f-27df-4f61-8755-262ec11af660
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185557c4b908780c09714aa9cc7fa4c80399812f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366022"
---
# <a name="access-point-initialization-of-eap"></a>Inicialização do ponto de acesso do EAP

Na inicialização, o AP (ponto de acesso) consulta o registro em busca de protocolos de autenticação instalados. Em seguida, o AP chama a função exportada [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) para cada protocolo de autenticação. A função **RasEapGetInfo** recebe um único parâmetro do tipo [**\_ \_ informações de EAP do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info). O AP usa o membro **dwEapTypeId** dessa estrutura para especificar o protocolo de autenticação. Observe que uma única DLL pode dar suporte a mais de um protocolo. Se **RasEapGetInfo** retornar qualquer valor diferente de **nenhum \_ erro**, o AP assumirá que o protocolo de autenticação não está disponível.

Em retorno de [**RasEapGetInfo**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetinfo) , a estrutura de [**\_ \_ informações de EAP do PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_info) contém ponteiros para as funções [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)), [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))e [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) na DLL de EAP. O serviço AP usa essas funções para interoperar com o protocolo de autenticação. O AP chama imediatamente **RasEapInitialize** para cada protocolo de autenticação, para inicializá-lo. Quando o serviço é desligado, ele chama **RasEapInitialize** novamente, desta vez com o parâmetro *FInitialize* definido como **false** para indicar que o protocolo de autenticação deve desligar.

 

 