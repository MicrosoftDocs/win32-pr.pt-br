---
description: Autenticação de origem da rede
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticação de origem da rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010665"
---
# <a name="network-source-authentication"></a>Autenticação de origem da rede

Alguns hosts de mídia podem exigir credenciais de usuário de aplicativos cliente antes de permitir o acesso à mídia. As credenciais do usuário incluem identificação e prova de identificação, como nome de usuário e senha, que são usados pelo servidor de mídia para conceder acesso à fonte de rede que hospeda. A fonte de rede pode fornecer autenticação NTLM, Digest ou básica.

Aplicativos baseados em Media Foundation podem armazenar credenciais de usuário para uma URL específica em um objeto de *credencial* que expõe a interface [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . O objeto Credential armazena credenciais criptografadas e fornece métodos para retornar informações como nome de usuário, senha e domínio.

Os objetos de credencial são criados e mantidos em um cache. O objeto de *cache de credencial* , exposto pela interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , fornece métodos para recuperar os objetos de credencial do cache de credenciais.

Um aplicativo que dá suporte à autenticação deve implementar a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Media Foundation não fornece uma implementação padrão dessa interface. O Gerenciador de credenciais é responsável por coletar as credenciais necessárias para uma URL da entrada do usuário ou leitura do armazenamento persistente.

Esta seção contém os seguintes tópicos:

-   [Configurando um Gerenciador de credenciais](setting-a-credential-manager.md)
-   [Usando o cache de credenciais](using-the-credential-cache.md)
-   [Implementando IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



