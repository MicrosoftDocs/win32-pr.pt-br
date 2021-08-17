---
description: Os provedores de serviços que suportam a abstração OOB (dados fora de banda) para os soquetes de estilo de fluxo devem aderir à semântica nesta seção.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Dados fora de banda na SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741043"
---
# <a name="out-of-band-data-in-the-spi"></a>Dados fora de banda na SPI

Os provedores de serviços que suportam a abstração OOB (dados fora de banda) para os soquetes de estilo de fluxo devem aderir à semântica nesta seção. Descreveremos o tratamento de dados OOB de maneira independente de protocolo. Consulte os Anexos [winsock para uma](winsock-annexes.md) discussão sobre os dados OOB implementados usando dados urgentes em provedores de serviços TCP/IP. A seguir, o uso de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) também se aplica a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
