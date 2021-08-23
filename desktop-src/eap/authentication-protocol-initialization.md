---
title: Inicialização do protocolo de autenticação
description: A conexão segura de EAP é inicializada entre o cliente e o servidor de maneiras semelhantes para clientes RAS e sem fio (802.1X).
ms.assetid: 1cd5bfc9-2ba3-477c-9bbb-73578a5623c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d53643718f747e1f39aaf68393f92a0577455041ec765ca19bea710f2c3aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984456"
---
# <a name="authentication-protocol-initialization"></a>Inicialização do protocolo de autenticação

A conexão segura de EAP é inicializada entre o cliente e o servidor de maneiras semelhantes para clientes RAS e sem fio (802.1X).

## <a name="client"></a>Cliente

Quando o cliente tenta estabelecer a conexão, o serviço de autenticação obtém [informações de identidade](obtaining-identity-information.md) para o usuário. Se o **valor DE INVOKE \_ \_ \_ \_ NAMEDLG DE RAS EAP VALUENAME** estiver presente no Registro para esse protocolo de autenticação e esse valor for definido como zero, o serviço de autenticação chamará [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). Essa função normalmente exibe uma interface do usuário que permite que as informações de identidade sejam de um tipo específico ao protocolo de autenticação; por exemplo, um certificado ou uma ID numérica. Se **RAS \_ EAP \_ VALUENAME INVOKE \_ \_ NAMEDLG** não estiver presente ou estiver definido como um, o serviço de autenticação exibirá a caixa de diálogo padrão nome de usuário do sistema.

Depois que o serviço de autenticação tiver obtido as informações de identidade do usuário, ele chamará a implementação do protocolo de autenticação [**rasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) Essa chamada permite que o protocolo de autenticação aloce e inicialize um buffer de trabalho que o serviço passa em chamadas subsequentes para [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) e [**RasEapEnd.**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) O buffer de trabalho é opaco para o serviço e nunca acessa o conteúdo do buffer de trabalho. Se o protocolo de autenticação criar um buffer de trabalho distinto para cada sessão EAP, o buffer de trabalho será de sessão e thread-safe. Como o protocolo de autenticação aloca a memória para o buffer de trabalho, o protocolo de autenticação também deve liberar essa memória usando a [**função RasEapFreeMemory.**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Na chamada para [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), o serviço também passa uma estrutura [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) que contém ponteiros para as informações de configuração para a conexão e as informações de identidade para o usuário. O serviço sempre passa um valor para o **membro pszIdentity** de **PPP \_ EAP \_ INPUT.** No entanto, **o membro pszPassword** de [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) pode ser **NULL.**

Dentro da estrutura [**PPP \_ EAP \_ INPUT,**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) o membro **fAuthenticator** indica se o protocolo de autenticação está sendo invocado para ser autenticado (no cliente) ou como o autenticador (no servidor).

## <a name="server"></a>Servidor

No servidor, o **membro bInitialID** de [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) especifica a ID que o servidor usa para o primeiro pacote EAP. O servidor incrementa essa ID para pacotes subsequentes.

Também no servidor, o ponteiro **pUserAttributes** em [**PPP \_ EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) aponta para uma matriz de atributos do tipo [**DE ATRIBUTO RAS \_ AUTH. \_ \_**](/windows/win32/api/raseapif/ne-raseapif-ras_auth_attribute_type) Esses são atributos para o usuário que foram obtidos do cliente.

Se a [**chamada RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) retornar qualquer valor diferente de **NO \_ ERROR,** a sessão será desconectada. O erro retornado é registrado (no servidor) ou exibido para o usuário (no cliente).

 

 