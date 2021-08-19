---
description: As classes RealTimeStylus, GestureRecognizer e DynamicRenderer são implementadas como wrappers COM e estão disponíveis apenas no código gerenciado.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Notas de implementação para as APIs StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032374"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Notas de implementação para as APIs StylusInput

As [**classes RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))e [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) são implementadas como wrappers COM e estão disponíveis somente no código gerenciado.

Quando o [**objeto RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))ou [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) é adicionado como um plug-in a um objeto **RealTimeStylus,** os objetos COM subjacentes interagem no nível COM. Portanto, não há suporte para chamar diretamente os métodos das interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) ou [IStylusAsyncPlugin.](/previous-versions/ms575194(v=vs.100)) Adicionar o **objeto RealTimeStylus**, GestureRecognizer ou DynamicRenderer ao **objeto RealTimeStylus** é a única maneira de acessar esses recursos.

 

 
