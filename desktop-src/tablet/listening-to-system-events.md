---
description: Os aplicativos podem escutar eventos do sistema usando o objeto InkCollector e ouvindo o evento SystemGesture nele.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ouvindo eventos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02d9d5ae20ac70e648071dfef904cb1ac7983c79c4aca3b02309ce1d20ac52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031814"
---
# <a name="listening-to-system-events"></a>Ouvindo eventos do sistema

Os aplicativos podem escutar eventos do sistema usando o objeto [**InkCollector**](inkcollector-class.md) e ouvindo o evento [**SystemGesture**](inkcollector-systemgesture.md) nele. Você pode definir quais eventos um aplicativo ouve. Quando ocorre uma ação da caneta do Tablet, o evento **SystemGesture** correspondente é enviado para o aplicativo em seu objeto **InkCollector** . Um aplicativo pode cancelar a mensagem do mouse que corresponde a um determinado evento **SystemGesture** quando recebe o evento. Para obter detalhes sobre como cancelar mensagens do mouse, consulte evento **SystemGesture** .

 

 



