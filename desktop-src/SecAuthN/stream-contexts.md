---
description: Os contextos de fluxo lidam com os protocolos seguros orientados a fluxo, como SSL ou PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contextos de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c843889df6aec3f82e8cb8516a7c23ccbf7a6de9957f9a0c572f6e6ca63ac75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916675"
---
# <a name="stream-contexts"></a>Contextos de fluxo

Os contextos de fluxo lidam com os protocolos seguros orientados a fluxo, como SSL ou PCT. No interesse de compartilhar a mesma interface e o gerenciamento de credenciais semelhante, o SSPI fornece suporte para contextos de fluxo. O [*protocolo de segurança*](../secgloss/s-gly.md) incorpora o esquema de autenticação do fluxo e os formatos de registro.

Para fornecer protocolos orientados a fluxo, os [*pacotes de segurança*](../secgloss/s-gly.md) que dão suporte a contextos de fluxo têm as seguintes características de processo:

-   O pacote define o \_ sinalizador de fluxo de sinalizador SECPKG \_ para indicar que ele dá suporte à semântica de fluxo.
-   Os aplicativos de transporte solicitam semânticas de fluxo Configurando os sinalizadores de fluxo de solicitações de transmissão e de transmissão do ISC \_ \_ \_ \_ nas chamadas para as funções [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
-   O aplicativo chama a função [**QueryContextAttributes (geral)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) com uma estrutura [**SecPkgContext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) para consultar o [*contexto de segurança*](../secgloss/s-gly.md) para o número de buffers a serem fornecidos e os tamanhos a serem reservados para cabeçalhos ou trailers.
-   O aplicativo fornece descritores de buffer para sobressalente durante o processamento real dos dados. Ao especificar a semântica de fluxo, o chamador indica a disposição para fazer processamento extra para que o [*pacote de segurança*](../secgloss/s-gly.md) possa lidar com o bloqueio das mensagens. Em essência, para as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , o chamador passa em uma lista de buffers. Quando uma mensagem é recebida de um canal que é orientado por fluxo (como uma porta TCP), o chamador passa em uma lista de buffers da seguinte maneira.

    | Buffer | Comprimento         | Tipo de buffer      |
    |--------|----------------|------------------|
    | 1      | Comprimento da mensagem | dados do SECBUFFER \_  |
    | 2      | 0              | SECBUFFER \_ vazio |
    | 3      | 0              | SECBUFFER \_ vazio |
    | 4      | 0              | SECBUFFER \_ vazio |
    | 5      | 0              | SECBUFFER \_ vazio |

    

     

    O pacote de segurança funciona no [*blob*](../secgloss/b-gly.md). Se a função retornar com êxito, a lista de buffers será parecida com a mostrada a seguir.

    

    | Buffer | Comprimento         | Tipo de buffer                |
    |--------|----------------|----------------------------|
    | 1      | Comprimento do cabeçalho  | \_cabeçalho de fluxo de SECBUFFER \_  |
    | 2      | Comprimento dos dados    | dados do SECBUFFER \_            |
    | 3      | Comprimento do trailer | \_trailer de fluxo de SECBUFFER \_ |
    | 4      | 0              | SECBUFFER \_ vazio           |
    | 5      | 0              | SECBUFFER \_ vazio           |

    

     

    O pacote também poderia retornar o buffer \# 4 com o comprimento x e o tipo de buffer SECBUFFER \_ extra indicando que os dados nesse buffer fazem parte do próximo registro e ainda não foram processados. Por outro lado, se a função Message retornar o \_ código de erro da mensagem s E \_ incompletas \_ , a lista de buffers retornada será parecida com a seguinte.

    

    | Buffer | Comprimento | Tipo de buffer        |
    |--------|--------|--------------------|
    | 1      | x      | SECBUFFER \_ ausente |

    

     

    Isso indica que mais dados foram necessários para processar o registro. Ao contrário da maioria dos erros retornados de uma função de mensagem, esse tipo de buffer não indica que o contexto foi comprometido. Em vez disso, ele indica que mais dados são necessários. os [*pacotes de segurança*](../secgloss/s-gly.md) não devem atualizar seu [*estado*](../secgloss/s-gly.md) nessa condição.

    Da mesma forma, no lado do remetente da comunicação, o chamador pode chamar a função [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) . O pacote de segurança pode precisar realocar o buffer ou copiar as coisas. O chamador pode ser mais eficiente fornecendo uma lista de buffers da seguinte maneira.

    

    | Buffer | Comprimento         | Type                       |
    |--------|----------------|----------------------------|
    | 1      | Comprimento do cabeçalho  | \_cabeçalho de fluxo de SECBUFFER \_  |
    | 2      | Comprimento dos dados    | dados do SECBUFFER \_            |
    | 3      | Comprimento do trailer | \_trailer de fluxo de SECBUFFER \_ |

    

     

    Isso permite que o chamador use os buffers com mais eficiência. Chamando a função [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) para determinar a quantidade de espaço a ser reservada antes de chamar [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), a operação é mais eficiente para o aplicativo e o pacote de segurança.

 

 
