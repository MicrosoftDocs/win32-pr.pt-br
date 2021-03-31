---
description: Esta \_ função TSPI lineSetCurrentLocation está obsoleta. A TAPI chamou essa função quando o usuário (usando a caixa de diálogo Propriedades de discagem) ou um aplicativo (usando a função lineSetCurrentLocation) alterou o local de conversão de endereço.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662323"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Esta \_ função TSPI lineSetCurrentLocation está obsoleta. A TAPI chamou essa função quando o usuário (usando a caixa de diálogo **Propriedades de discagem** ) ou um aplicativo (usando a função [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) alterou o local de conversão de endereço.

Atualmente, uma alteração no local de tradução resulta em uma \_ mensagem DEVSTATE de linha com *dwParam1* definido como LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
