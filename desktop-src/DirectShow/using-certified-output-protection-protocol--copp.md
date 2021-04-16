---
description: Usando o protocolo COPP (certificado de proteção de saída)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Usando o protocolo COPP (certificado de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786963"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Usando o protocolo COPP (certificado de proteção de saída)

O protocolo COPP (certificado de proteção de saída) permite que um aplicativo proteja um fluxo de vídeo à medida que ele viaja do adaptador gráfico para o dispositivo de vídeo. Um aplicativo pode usar COPP para descobrir que tipo de conector físico está anexado ao dispositivo de vídeo e quais tipos de proteção de saída estão disponíveis. Os mecanismos de proteção incluem o seguinte:

-   Proteção de Conteúdo Digital High-Bandwidth (HDCP)
-   Sistema de gerenciamento de geração de cópia — analógico (CGMS-A)
-   Proteção de cópia analógica (ACP)

Se o adaptador gráfico oferecer suporte a um desses mecanismos, o aplicativo poderá usar COPP para definir o nível de proteção.

COPP define um protocolo que é usado para estabelecer um canal de comunicações seguro com o driver de gráficos. Ele usa MACs (códigos de autenticação de mensagens) para verificar a integridade dos comandos COPP que são passados entre o aplicativo e o driver de vídeo. O aplicativo usa COPP chamando métodos na interface [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) do filtro de processador de mixagem de vídeo do DIRECTSHOW (VMR-7 ou VMR-9).

A COPP não define nada sobre as políticas de direitos digitais que podem ser aplicadas ao conteúdo de mídia digital. Além disso, a própria COPP não implementa sistemas de proteção de saída. O protocolo COPP simplesmente fornece uma maneira de definir e consultar os níveis de proteção no adaptador gráfico, usando os sistemas de proteção fornecidos pelo adaptador.

Esta seção pressupõe que você esteja familiarizado com as seguintes tecnologias:

-   DirectShow
-   SDK do Windows Media Format
-   XML
-   Criptografia de chave pública e criptografia simétrica

Os exemplos de código nesta seção usam o CryptoAPI da Microsoft para executar operações criptográficas. Esta seção contém os seguintes tópicos:

-   [Visão geral de COPP](overview-of-copp.md)
-   [Obtendo a cadeia de certificados do driver](obtaining-the-drivers-certificate-chain.md)
-   [Validando a cadeia de certificados](validating-the-certificate-chain.md)
-   [Listas de certificados revogados](certificate-revocation-lists.md)
-   [Importando a chave pública do driver](importing-the-drivers-public-key.md)
-   [Iniciando uma sessão COPP](initiating-a-copp-session.md)
-   [Enviando solicitações de status COPP](sending-copp-status-requests.md)
-   [Enviando comandos COPP](sending-copp-commands.md)
-   [Testando se um driver gráfico dá suporte a COPP](testing-whether-a-graphics-driver-supports-copp.md)
-   [Referência de consulta COPP](copp-query-reference.md)
-   [Referência de comando COPP](copp-command-reference.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o processador de mixagem de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



