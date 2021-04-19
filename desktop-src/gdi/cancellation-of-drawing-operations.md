---
description: Quando aplicativos de desenho complexos executam operações de gráficos demoradas, eles consomem recursos valiosos do sistema.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Cancelamento de operações de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988839"
---
# <a name="cancellation-of-drawing-operations"></a>Cancelamento de operações de desenho

Quando aplicativos de desenho complexos executam operações de gráficos demoradas, eles consomem recursos valiosos do sistema. Aproveitando os recursos de multitarefa do sistema, um aplicativo pode usar threads e a função [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) para gerenciar essas operações. Por exemplo, se a operação gráfica executada pelo thread A estiver consumindo os recursos necessários, o thread B poderá chamar a função CancelDC para interromper essa operação.

 

 



