---
title: Classe CSecureChannelClient
description: Classe CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Mídia Gerenciador de Dispositivos, classe CSecureChannelClient
- Gerenciador de Dispositivos, classe CSecureChannelClient
- aplicativos de área de trabalho, classe CSecureChannelClient
- referência de programação, classe CSecureChannelClient
- referência para Windows Media Gerenciador de Dispositivos, classe CSecureChannelClient
- Classe CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef469c1e7a73b04124850952ef0690bd18c82ecb3fc624d08df081b7b669637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585609"
---
# <a name="csecurechannelclient-class"></a>Classe CSecureChannelClient

A classe **CSecureChannelClient** é uma classe auxiliar (não uma interface) que permite que os aplicativos se autentiquem, criptografem e descriptografem dados e criem Macs.

A classe **CSecureChannelClient** expõe os métodos a seguir.



| Método                                                            | Descrição                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autenticar**](/previous-versions/ms983906(v=msdn.10))         | Dispara a troca de certificados entre componentes para estabelecer confiança.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Descriptografa os dados recebidos por meio de um parâmetro.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Criptografa os dados sendo enviados por meio de um parâmetro.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Verifica se um canal de autenticação segura foi estabelecido com êxito. Esse método não é usado por aplicativos. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Recupera os níveis de segurança do aplicativo dos componentes locais e remotos.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Recupera a chave de sessão atual. Esse método não é usado por aplicativos.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Libera o canal do código de autenticação de mensagem (MAC) e recupera um valor MAC final.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Adquire um canal MAC (código de autenticação de mensagens).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Adiciona um valor a um MAC (código de autenticação de mensagem).                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Especifica o certificado e a chave privada do cliente do (a) canal autenticado seguro (SAC).                               |
| [**Setinterface**](/previous-versions/bb231595(v=vs.85))         | Seleciona a interface usada para comunicações de canal autenticado seguro (SAC).                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Define a chave de sessão que é usada para se comunicar com outro componente. Esse método não é usado por aplicativos.         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CSecureChannelServer**](csecurechannelserver-class.md)
</dt> <dt>

[**Interface IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces para aplicativos**](interfaces-for-applications.md)
</dt> </dl>

 

 