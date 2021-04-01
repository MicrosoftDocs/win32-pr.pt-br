---
title: Chamadas aninhadas para SRSetRestorePoint
description: Este tópico descreve o suporte para chamadas aninhadas para SRSetRestorePoint por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159916"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Chamadas aninhadas para SRSetRestorePoint

Este tópico descreve o suporte para chamadas aninhadas para [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .

Os aplicativos podem chamar [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com segurança ao usar esses tipos de evento. A primeira chamada para a função cria um ponto de restauração. As chamadas aninhadas subsequentes para a função não criam pontos de restauração. Por exemplo, suponha que um aplicativo faça as seguintes chamadas para **SRSetRestorePoint**:<dl> Para o ponto de restauração A com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração B com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração B com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração A com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_  
</dl>

A segunda chamada não cria um novo ponto de restauração porque a chamada está aninhada.

 

 




