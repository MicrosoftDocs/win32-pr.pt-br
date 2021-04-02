---
description: A semântica para contextos de datagramas ou sem conexão é ligeiramente diferente daquela para contextos orientados a conexão.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextos de datagrama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090760"
---
# <a name="datagram-contexts"></a>Contextos de datagrama

A semântica para contextos de [*datagramas*](/windows/desktop/SecGloss/d-gly)ou sem conexão é ligeiramente diferente daquela para contextos orientados a conexão. No [*contexto*](/windows/desktop/SecGloss/c-gly)sem conexão de um datagrama, um servidor não pode determinar quando o cliente foi desligado ou, de outra forma, terminou a conexão. Em outras palavras, nenhum aviso de encerramento é passado do aplicativo de transporte para o servidor, como ocorreria em um contexto orientado a conexão.

Para usar um contexto de datagrama, um cliente define o \_ sinalizador de datagrama de req do ISC \_ em sua chamada para a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

> [!IMPORTANT]
> O pacote [Kerberos da Microsoft](microsoft-kerberos.md) não oferece suporte a contextos de datagrama no modo de usuário para usuário.

 

Para oferecer melhor suporte a alguns modelos, especialmente o RPC no estilo DCE, as seguintes regras se aplicam quando o cliente usa um contexto de datagrama:

-   O [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) não produz um [*blob*](/windows/desktop/SecGloss/b-gly) de autenticação (objeto binário grande) na primeira chamada para [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). No entanto, o cliente pode usar o contexto de segurança retornado em uma chamada para a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para gerar uma assinatura para uma mensagem.
-   O pacote de segurança deve permitir que o contexto seja restabelecido várias vezes para permitir que o servidor descarte a conexão sem aviso prévio. Isso implica que todas as chaves usadas nas funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) podem ser redefinidas para um [*estado*](/windows/desktop/SecGloss/s-gly)consistente.
-   O pacote de segurança permite que o chamador Especifique informações de sequência e forneça essas informações de sequência no lado do destinatário. Isso é além das informações de sequência mantidas pelo pacote.

Um pacote de segurança define o \_ sinalizador de datagrama de sinalizador SECPKG \_ para indicar que ele dá suporte à semântica de datagrama.

 

 
