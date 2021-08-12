---
title: Classe CSecureChannelServer
description: Classe CSecureChannelServer
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Gerenciador de Dispositivos,classe CSecureChannelServer
- Gerenciador de Dispositivos,classe CSecureChannelServer
- provedores de serviços, classe CSecureChannelServer
- referência de programação, classe CSecureChannelServer
- referência para Windows media Gerenciador de Dispositivos, classe CSecureChannelServer
- Classe CSecureChannelServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87627fcdee6da42927ab88411dd579225dc38f025ae73bf9f4fe787c0c5e44bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585480"
---
# <a name="csecurechannelserver-class"></a>Classe CSecureChannelServer

A classe **CSecureChannelServer** é uma classe auxiliar (não uma interface) que permite a um provedor de serviços ou provedor de conteúdo seguro autenticar um aplicativo usando a interface [**IComponentAuthenticate,**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) criptografar e descriptografar dados e criar assinaturas MAC. O processo de autenticação requer que o aplicativo crie um **objeto CSecureChannelClient** e que o provedor de serviços crie um **objeto CSecureChannelServer.** As **classes CSecureChannelClient** e **CSecureChannelServer** são declaradas na biblioteca de link estático, Mssachlp.lib. Todos os métodos de Windows media Gerenciador de Dispositivos, provedor de serviços e interfaces de provedor de conteúdo seguro podem retornar WMDM E NOTCERTIFIED para indicar que o chamador não foi autenticado com \_ \_ êxito.

A **classe CSecureChannelServer** expõe os métodos a seguir.



| Método                                                            | Descrição                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Descriptografa os dados contidos em um parâmetro.                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Criptografa os dados contidos em um parâmetro.                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Verifica se um canal de autenticação seguro foi estabelecido com êxito.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Recupera os níveis de segurança do aplicativo dos componentes locais e remotos.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Recupera a chave de sessão atual.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Libera o canal mac (código de autenticação de mensagem) e recupera um valor mac final.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Adquire um canal mac (código de autenticação de mensagem).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Atualiza o valor do MAC (código de autenticação de mensagem) com um valor de parâmetro.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Estabelece um canal autenticado seguro entre componentes.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Relata os protocolos com suporte de um componente.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Especifica o certificado e a chave privada do servidor SAC (canal autenticado seguro). |
| [**Setsessionkey**](/previous-versions/ms868519(v=msdn.10))       | Define a chave de sessão usada para se comunicar com outro componente.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CSecureChannelClient**](csecurechannelclient-class.md)
</dt> <dt>

[**IComponentAuthenticate Interface**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces para provedores de serviços**](interfaces-for-service-providers.md)
</dt> <dt>

[**Usando canais autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 