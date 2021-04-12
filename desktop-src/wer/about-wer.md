---
title: Sobre o WER
description: O Relatório de Erros do Windows (WER) é uma infra-estrutura de comentários flexível baseada em eventos, criada para coletar informações sobre os problemas de hardware e software que o Windows pode detectar, relatar as informações à Microsoft e fornecer aos usuários qualquer solução disponível. Para obter informações sobre os aprimoramentos do WER, consulte What ' s New in WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Relatório de Erros do Windows de relatório de erros do Windows, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292415"
---
# <a name="about-wer"></a>Sobre o WER

O Relatório de Erros do Windows (WER) é uma infra-estrutura de comentários flexível baseada em eventos, criada para coletar informações sobre os problemas de hardware e software que o Windows pode detectar, relatar as informações à Microsoft e fornecer aos usuários qualquer solução disponível. Para obter informações sobre os aprimoramentos do WER, consulte [What ' s New in WER](what-s-new-in-wer.md).

A partir do Windows Vista, o Windows fornece falha, sem resposta e relatório de erros de falha do kernel por padrão, sem a necessidade de alterações no seu aplicativo. Em vez disso, os aplicativos usam a API WER para gerar relatórios de erros para problemas específicos do aplicativo que não estão relacionados a falhas, não respostas ou falha do kernel.

Para gerar relatórios de erros para problemas específicos do aplicativo, o aplicativo deve criar uma breve descrição do problema usando algumas partes básicas de informações denominadas *parâmetros de relatório*. Os parâmetros de relatório incluem informações como o nome do aplicativo, a versão do aplicativo, o nome do módulo, a versão do módulo e o código de erro. A combinação desses parâmetros de relatório descreve um problema exclusivo.

Quando o WER verifica uma solução, ele se comunica com o servidor WER na Microsoft perguntando primeiro se o problema já é conhecido. O servidor responde de uma das seguintes maneiras:

-   Se o problema for conhecido e houver uma solução, o servidor enviará a solução para o computador cliente e o WER exibirá essas informações para o usuário.
-   Se o problema estiver sendo investigado, o servidor poderá enviar uma resposta que indica o status. Se o desenvolvedor precisar de mais informações para resolver o problema, o servidor solicitará informações adicionais do WER e o WER solicitará permissão ao usuário para enviar essas informações.
-   Se o problema não for conhecido, o servidor criará um problema para um desenvolvedor investigar e enviar uma resposta de WER que indica o status.

Usando esse processo, o WER coleta mais informações, se necessário, ou envia uma solução para o usuário quando disponível. No Windows Vista, o usuário pode ir para **relatórios de problemas e soluções** a qualquer momento para exibir as soluções disponíveis, verificar se novas soluções estão disponíveis ou gerenciar seus outros relatórios e configurações do WER. No Windows 7, os **relatórios de problemas e as soluções** agora são chamados de **central de ações**. Clique **em Iniciar** e digite "exibir" em **Pesquisar programas e arquivos** e, em seguida, selecione **Exibir todos os relatórios de problemas**, **Exibir histórico de confiabilidade** ou **Exibir soluções para problemas**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Relatório de Erros do Windows](windows-error-reporting.md)
</dt> </dl>

 

 




