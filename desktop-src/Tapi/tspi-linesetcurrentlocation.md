---
description: Essa função TSPI \_ lineSetCurrentLocation está obsoleta. TAPI chamou essa função quando o usuário (usando a caixa de diálogo Propriedades de Discagem) ou um aplicativo (usando a função lineSetCurrentLocation) alterou o local de conversão de endereços.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012116"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Essa função TSPI \_ lineSetCurrentLocation está obsoleta. TAPI chamou essa função quando  o usuário (usando a caixa de diálogo Propriedades de Discagem) ou um aplicativo (usando a função [**lineSetCurrentLocation)**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) alterou o local de conversão de endereços.

Atualmente, uma alteração no local de tradução resulta em uma mensagem LINE \_ DEVSTATE com *dwParam1* definido como LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
