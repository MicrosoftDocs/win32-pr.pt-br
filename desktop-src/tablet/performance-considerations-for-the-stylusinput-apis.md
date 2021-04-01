---
description: Descrição de maneiras de melhorar o desempenho ao usar as APIs (interfaces de programação de aplicativo) do StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerações sobre desempenho para a API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663257"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Considerações sobre desempenho para a API StylusInput

A lista a seguir descreve algumas maneiras de melhorar o desempenho de aplicativos que usam as APIs do StylusInput.

-   Use a propriedade [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) ou [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) para assinar apenas os dados relevantes para o seu plug-in. Isso reduz o número total de chamadas de método que o objeto [**RealTimeStylus**](realtimestylus-class.md) faz e também reduz a complexidade do seu plug-in. O objeto **RealTimeStylus** apenas verifica a propriedade DataInterest quando o plug-in é anexado.
-   Minimize a complexidade dos plug-ins síncronos. Plug-ins síncronos geralmente chamados pelo thread do objeto [**RealTimeStylus**](realtimestylus-class.md) e podem contribuir para atrasos na coleta de tinta.
-   Considere tornar seu plug-in assíncrono. Se o seu plug-in for complexo e precisar adicionar dados personalizados à fila do objeto [**RealTimeStylus**](realtimestylus-class.md) , considere usar um modelo **RealTimeStylus** em cascata e adicionar o plug-in à coleção de plug-ins síncrona do objeto **RealTimeStylus** secundário. Para obter mais informações sobre o modelo **RealTimeStylus** em cascata, consulte [o modelo RealTimeStylus em cascata](the-cascaded-realtimestylus-model.md).

 

 
