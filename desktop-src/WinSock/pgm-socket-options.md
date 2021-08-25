---
description: O PGM usa opções de soquete para definir o estado, fornecer parâmetros de multicast e, de outra forma, implementar seus recursos de multicast.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opções de soquete PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e8df8050146774ac79d45594adcccf53a93d295ce42b9f00834aa0d699e83a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860816"
---
# <a name="pgm-socket-options"></a>Opções de soquete PGM

O PGM usa opções de soquete para definir o estado, fornecer parâmetros de multicast e, de outra forma, implementar seus recursos de multicast. Esta página especifica como as opções de soquete PGM devem ser definidas, enumera as opções de soquete disponíveis para PGM e, quando apropriado, fornece exemplos de uso e informações adicionais para várias opções. Para obter as definições básicas de cada opção de soquete PCM, consulte [Opções de soquete](socket-options.md).

**Windows XP:** Não há suporte para a programação de multicast confiável (PGM).

As seguintes opções de soquete estão disponíveis para os remetentes do PGM:

<dl> \_LATEJOIN RM  
\_tamanho da \_ janela de taxa do RM \_  
\_taxa de \_ avçd da janela de envio do RM \_ \_  
\_estatísticas do remetente do RM \_  
\_ \_ método Advance da janela do remetente do \_ RM \_  
\_ \_ mcast TTL do conjunto do RM \_  
\_limite de \_ mensagem do conjunto do RM \_  
RM \_ set \_ Send \_ If  
RM \_ usar \_ FEC  
</dl>

A \_ opção método Advance de janela do remetente do RM \_ \_ \_ especifica o método usado ao avançar a janela de envio de borda à direita. O parâmetro optval só pode ser E \_ \_ de janela antecipada \_ por \_ hora (o padrão). Observe que \_ \_ \_ \_ \_ não há suporte para o uso da janela e como cache de dados.

As seguintes opções de soquete estão disponíveis para receptores PGM:

<dl> \_Adicionar recebimento de RM \_ \_ If  
recebimento do RM \_ del \_ \_ se  
\_consentimento de intranet de alta velocidade do RM \_ \_ \_  
\_estatísticas do receptor do RM \_  
</dl>

## <a name="setting-pgm-socket-options"></a>Definindo opções de soquete PGM

O trecho de código a seguir ilustra uma diretriz de programação para definir opções de soquete PGM:


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



No trecho acima, o tipo e o conteúdo de *OptionData* são dependentes da opção de soquete que está sendo definida. Para todas as opções de soquete PGM, o nível de soquete é IPPROTO \_ RM. As opções de soquete PGM devem ser definidas imediatamente após a chamada para a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , com as seguintes exceções:

<dl> \_limite de \_ mensagem do conjunto do RM \_  
\_estatísticas do remetente do RM \_  
\_estatísticas do receptor do RM \_  
</dl>

 

 



