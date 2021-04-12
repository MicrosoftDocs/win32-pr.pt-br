---
title: Configuração de autenticação dinâmica
description: Os aplicativos podem alterar as configurações de autenticação em um grupo de URLs ou sessão de servidor a qualquer momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291913"
---
# <a name="dynamic-authentication-configuration"></a>Configuração de autenticação dinâmica

Por padrão, a API do servidor HTTP não executa a autenticação, a menos que o aplicativo a habilite especificamente. Os aplicativos podem alterar as configurações de autenticação em um grupo de URLs ou sessão de servidor a qualquer momento. As alterações na configuração de autenticação não afetam as solicitações que já foram autenticadas ou que estão sendo expedidas para o aplicativo

Para esquemas de autenticação em que são necessários vários arredondamentos de handshake, a API do servidor HTTP descarta o handshake de autenticação se o esquema atual não tiver mais suporte devido a alterações de configuração do aplicativo. Por exemplo, se o aplicativo habilitar Negotiate e desabilitar o NTLM, e a API do servidor HTTP estiver no handshake de autenticação intermediária para NTLM, o handshake para NTLM será descartado e a solicitação será passada para o aplicativo. O aplicativo envia um desafio de autenticação 401 com os novos tipos de autenticação especificados no cabeçalho WWW-Authenticate.

 

 




