---
description: Atualmente, todo o tempo de chamadas é deixado para aplicativos.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Temporizador de estado de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754201"
---
# <a name="call-state-timer"></a>Temporizador de estado de chamada

Atualmente, todo o tempo de chamadas é deixado para aplicativos. Isso pode ser um tanto cansativo se o aplicativo estiver monitorando um grande número de chamadas, e se vários aplicativos estiverem presentes, possivelmente em vários servidores, poderá ser necessário para todos eles manter temporizadores nas mesmas chamadas. Portanto, faz mais sentido para o tempo de estado de chamada ser manipulado pelo servidor.

O membro **tStateEntryTime** no [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) permite o tempo de chamadas em Estados a serem relatados. O membro (do tipo **SYSTIME**) indica a hora em que o estado atual foi inserido.

 

 



