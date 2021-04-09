---
description: Os aplicativos podem escutar eventos do sistema usando o objeto InkCollector e ouvindo o evento SystemGesture nele.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Ouvindo eventos do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011772"
---
# <a name="listening-to-system-events"></a>Ouvindo eventos do sistema

Os aplicativos podem escutar eventos do sistema usando o objeto [**InkCollector**](inkcollector-class.md) e ouvindo o evento [**SystemGesture**](inkcollector-systemgesture.md) nele. Você pode definir quais eventos um aplicativo ouve. Quando ocorre uma ação da caneta do Tablet, o evento **SystemGesture** correspondente é enviado para o aplicativo em seu objeto **InkCollector** . Um aplicativo pode cancelar a mensagem do mouse que corresponde a um determinado evento **SystemGesture** quando recebe o evento. Para obter detalhes sobre como cancelar mensagens do mouse, consulte evento **SystemGesture** .

 

 



