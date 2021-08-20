---
title: Configuração de Autenticação Dinâmica
description: Os aplicativos podem alterar as configurações de autenticação em um Grupo de URL ou sessão de servidor a qualquer momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fda33e150826ed7d84ac45c4ab0771136991aa9aeb2766d5d395a65da270775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014834"
---
# <a name="dynamic-authentication-configuration"></a>Configuração de Autenticação Dinâmica

Por padrão, a API do Servidor HTTP não executa a autenticação, a menos que o aplicativo a habilita especificamente. Os aplicativos podem alterar as configurações de autenticação em um Grupo de URL ou sessão de servidor a qualquer momento. As alterações na configuração de autenticação não afetam solicitações que já estão autenticadas ou que estão sendo expedidas para o aplicativo

Para esquemas de autenticação em que várias rodadas de handshake são necessárias, a API do servidor HTTP descarta o handshake de autenticação se o esquema atual não tiver mais suporte devido a alterações de configuração do aplicativo. Por exemplo, se o aplicativo habilitar Negotiate e desabilitar o NTLM e a API do Servidor HTTP estiver no handshake de autenticação intermediária para NTLM, o handshake para NTLM será descartado e a solicitação será passada para o aplicativo. O aplicativo envia um desafio de autenticação 401 com os novos tipos de autenticação especificados no WWW-Authenticate de dados.

 

 




