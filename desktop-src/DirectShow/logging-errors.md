---
description: Erros de log
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Erros de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7402ade284f0d9a71b032f233276277dfdcd8c5e2844c85f03782caed101d095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685146"
---
# <a name="logging-errors"></a>Erros de log

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

os [serviços de edição de DirectShow](directshow-editing-services.md) (DES) fornecem um mecanismo interno para registrar erros que ocorrem durante o carregamento, a construção ou a renderização de um projeto DES. Este artigo apresenta um exemplo de aplicativo de console que carrega um arquivo de projeto XML e tenta renderizá-lo. Se ocorrer um erro, o aplicativo imprime uma mensagem de erro na janela do console. O código de exemplo apresentado neste artigo baseia-se no exemplo fornecido em [carregando e visualizando um Project](loading-and-previewing-a-project.md).

> [!Note]  
> Seu aplicativo não é necessário para implementar o log de erros. O DES não registra erros a menos que você solicite-o explicitamente.

 

Este artigo pressupõe que você entende a programação de cliente COM e o modelo de linha do tempo DES. Além disso, você precisa entender os conceitos básicos da programação de objetos COM. Para obter informações sobre cronogramas em DES, consulte [o modelo de linha do tempo](the-timeline-model.md).

Este artigo inclui as seções a seguir.

-   [Visão geral do log de erros](overview-of-error-logging.md)
-   [Criando uma classe de log de erros](creating-an-error-logging-class.md)
-   [Implementando IAMErrorLog](implementing-iamerrorlog.md)
-   [Configurando o log de erros](setting-the-error-log.md)
-   [Log de erros DES: código de exemplo](des-error-logging--example-code.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[usando DirectShow serviços de edição](using-directshow-editing-services.md)
</dt> </dl>

 

 



