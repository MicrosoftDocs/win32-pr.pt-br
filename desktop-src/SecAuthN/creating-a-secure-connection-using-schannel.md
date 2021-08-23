---
description: Como criar uma conexão segura usando Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Criando uma conexão segura usando Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374955b67bfa0026da5e8f8e9e88ce71da24231e218cb869cb532d05d4171bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008904"
---
# <a name="creating-a-secure-connection-using-schannel"></a>Criando uma conexão segura usando Schannel

O [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) Schannel fornece acesso a quatro [*protocolos de segurança*](/windows/desktop/SecGloss/s-gly):

-   [Segurança de camada de transporte (TLS 1,2)](transport-layer-security-protocol.md)
-   [Segurança de camada de transporte (TLS 1,1)](transport-layer-security-protocol.md)
-   [Segurança de camada de transporte (TLS 1,0)](transport-layer-security-protocol.md)
-   [Protocolo SSL (SSL 3,0)](secure-sockets-layer-protocol.md)
-   [Protocolo SSL (SSL 2,0)](secure-sockets-layer-protocol.md)

> [!Note]  
> Os protocolos PCT e SSL 2,0 foram substituídos pelo protocolo TLS e não devem ser usados para um novo desenvolvimento.

 

**Para configurar uma conexão segura entre um cliente e um servidor**

1.  Obter credenciais do Schannel ([obtendo credenciais Schannel](obtaining-schannel-credentials.md)).
2.  Criar um contexto de segurança Schannel ([criando um contexto de segurança Schannel](creating-an-schannel-security-context.md)).

Depois que uma conexão é estabelecida, você pode recuperar informações sobre seus atributos. Para obter detalhes, consulte [obtendo informações sobre conexões Schannel](getting-information-about-schannel-connections.md).

Se, depois de estabelecer uma conexão, os requisitos de segurança do aplicativo forem alterados ou a conexão for perdida, você poderá renegociar a conexão. Para obter detalhes, consulte [renegociando uma conexão Schannel](renegotiating-an-schannel-connection.md).

Quando terminar de usar uma conexão Schannel, você deverá executar a limpeza necessária. Para obter detalhes, consulte [desligando uma conexão Schannel](shutting-down-an-schannel-connection.md).

Para obter informações sobre exemplos fornecidos com o SDK (Software Development Kit) da plataforma que demonstram o [*pacote de segurança*](/windows/desktop/SecGloss/s-gly)Schannel, consulte os exemplos de PSDK usando Schannel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
