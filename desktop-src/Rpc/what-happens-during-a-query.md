---
title: O que acontece durante uma consulta
description: Esta seção descreve como a rede lida com a consulta quando um cliente de 32 bits procura um nome em seu próprio domínio.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159870"
---
# <a name="what-happens-during-a-query"></a>O que acontece durante uma consulta

Esta seção descreve como a rede lida com a consulta quando um cliente de 32 bits procura um nome em seu próprio domínio.

Quando o aplicativo cliente chama [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), o localizador que reside no computador cliente tentará atender a essa solicitação. Se não houver nada no cache, ele encaminhará a solicitação por RPC para um localizador mestre. Se o localizador mestre não encontrar nada em seu cache, ele enviará a solicitação para todos os computadores no domínio usando uma difusão de slot de email. Se houver uma correspondência, o localizador em cada computador responderá por um slot de email direcionado. (Por exemplo, se um processo nesse computador tiver exportado a interface.) As respostas são agrupadas e o RPC é concluído do localizador de processo do cliente, que responderá ao próprio processo do cliente.

Em um domínio, o localizador de cliente procura um localizador mestre nos seguintes locais:

-   No controlador de domínio primário
-   Em cada controlador de domínio de backup

Se uma correspondência não for encontrada, o localizador do cliente se declarará para ser o localizador mestre. Como tal, ele transmitirá consultas se elas não puderem ser atendidas localmente.

Em um grupo de trabalho, o localizador de cliente mantém um cache dos computadores cujos localizadores têm difusão. Ele usa aquele que está executando o mais longo que o localizador mestre. Se esse computador não estiver disponível, o próximo computador de difusão mais longa será usado e assim por diante. Se o cliente precisar de um localizador mestre e o cache estiver vazio, ele reabastecerá o cache enviando uma difusão especial de slot de email que solicita aos localizadores mestres a resposta. Se não houver respostas, o localizador do cliente se declarará para ser o localizador mestre e transmitirá as consultas se elas não puderem ser satisfeitas localmente.

Isso mudará se o aplicativo cliente for um programa baseado em 16 bits ou em MS-dos. Nesse caso, não há nenhum localizador em execução no computador cliente e Rpcns1.dll ou Rpcnslm. RPC contém o código para localizar um localizador mestre. Todas as solicitações são encaminhadas diretamente para o localizador mestre.

Essas diretrizes são válidas para nomes no domínio do cliente, como nomes de "/.:/ entryname ". Se o cliente solicitar um nome de outro domínio por meio do uso de "/.../DOMAIN/entryname;", o localizador de cliente encaminhará a solicitação para o domínio especificado, que a transmitirá se não tiver a resposta. Se o domínio estiver inoperante ou for realmente um grupo de trabalho, a solicitação falhará.

> [!Note]  
> Lembre-se do seguinte ao trabalhar com entradas no serviço de nome:

 

-   Um cliente não pode usar a sintaxe "/.../DOMAIN/entryname" para localizar uma entrada em seu próprio domínio. Use a sintaxe "/.:/ entryname ". No entanto, você pode usar "/.../DOMAIN/entryname" para localizar uma entrada em outro domínio.
-   O nome de domínio em "/.../DOMAIN/entryname" deve estar em letras maiúsculas. Ao procurar uma correspondência, o localizador diferencia maiúsculas de minúsculas.
-   Os nomes de entrada do localizador também diferenciam maiúsculas de minúsculas, mas não precisam ser maiúsculos.
-   Quando o cliente usa o "/.:/ entryname ", o localizador não pesquisará entradas em outros domínios, mesmo que tenham uma relação de confiança com o domínio de logon.
-   Difusões não cruzam segmentos de LAN (por exemplo, sub-redes). Portanto, a utilidade do localizador é limitada em uma organização com várias sub-redes.

 

 




