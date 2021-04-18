---
description: A lista a seguir contém as metas de design TAPI MSP.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Metas gerais de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761967"
---
# <a name="general-design-goals"></a>Metas gerais de design

A lista a seguir contém as metas de design TAPI MSP.

-   As classes base foram mantidas simples, com membros e métodos introduzidos apenas quando absolutamente necessário.
-   Herança simples. Não há várias heranças entre classes, embora várias heranças sejam usadas para as interfaces.
-   O bloqueio ocorre apenas em uma direção para evitar o deadlock. Os métodos no objeto de chamada que exigem o bloqueio na chamada podem chamar métodos no fluxo que exigem o bloqueio no fluxo. No entanto, os métodos no fluxo que exigem o bloqueio no fluxo nunca chamarão um método na chamada que exige um bloqueio na chamada.
-   RefCounts são usados para proteger o acesso. Todos os retornos de chamada postados no pool de threads contêm refCounts. O Refcount é cancelado quando a espera é cancelada. O objeto de endereço tem refCounts nos terminais. Os objetos de chamada têm refCounts no endereço e em fluxos. Os objetos de fluxo têm refCounts em chamadas e terminais. Os terminais têm refCounts em fluxos. A quebra de refCounts circular quando o método de desligamento nos objetos address e Call é chamado.

 

 



