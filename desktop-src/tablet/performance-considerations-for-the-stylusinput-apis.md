---
description: Descrição de maneiras de melhorar o desempenho ao usar as APIs (interfaces de programação de aplicativo) StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerações de desempenho para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef40ab389687cd42ef516a61f61ab86a7eb79d4efac9ae6e9dd698e93e54bff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856488"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Considerações de desempenho para a API StylusInput

A lista a seguir descreve algumas maneiras de melhorar o desempenho de aplicativos que usam as APIs StylusInput.

-   Use a [propriedade Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) ou [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) para assinar somente os dados relevantes para o plug-in. Isso reduz o número geral de chamadas de método que o objeto [**RealTimeStylus**](realtimestylus-class.md) faz e também reduz a complexidade do plug-in. O **objeto RealTimeStylus** verifica apenas a propriedade DataInterest quando o plug-in é anexado.
-   Minimize a complexidade de plug-ins síncronos. Plug-ins síncronos geralmente chamados pelo thread do objeto [**RealTimeStylus**](realtimestylus-class.md) e podem contribuir com atrasos na coleta de tinta.
-   Considere tornar seu plug-in assíncrono. Se o plug-in for complexo e precisar adicionar dados personalizados à fila do objeto [**RealTimeStylus,**](realtimestylus-class.md) considere usar um modelo **realTimeStylus** em cascata e adicionar o plug-in à coleção de plug-in síncrona do objeto **RealTimeStylus** secundário. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte O modelo [RealTimeStylus](the-cascaded-realtimestylus-model.md)em cascata .

 

 
