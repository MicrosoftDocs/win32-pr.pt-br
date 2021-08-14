---
title: Chamadas aninhadas para SRSetRestorePoint
description: Este tópico descreve o suporte para chamadas aninhadas para SRSetRestorePoint por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12286a69bdb83cb5fd119280e8996c6612e359bf93b9371b6a088a98bf6fd881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857631"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Chamadas aninhadas para SRSetRestorePoint

Este tópico descreve o suporte para chamadas aninhadas para [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) por meio dos \_ tipos de evento iniciar alteração do sistema aninhado \_ \_ e encerrar \_ alteração do sistema aninhado \_ \_ .

Os aplicativos podem chamar [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) com segurança ao usar esses tipos de evento. A primeira chamada para a função cria um ponto de restauração. As chamadas aninhadas subsequentes para a função não criam pontos de restauração. Por exemplo, suponha que um aplicativo faça as seguintes chamadas para **SRSetRestorePoint**:<dl> Para o ponto de restauração A com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração B com dwEventType = iniciar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração B com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_  
Para o ponto de restauração A com dwEventType = encerrar \_ alteração do sistema aninhado \_ \_  
</dl>

A segunda chamada não cria um novo ponto de restauração porque a chamada está aninhada.

 

 




