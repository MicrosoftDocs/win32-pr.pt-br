---
title: Gravando dados usando um canal DVC
description: Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058235"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Gravando dados usando um canal DVC

Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente. A gravação de dados do canal é implementada pelo método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) da interface [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .

A ilustração a seguir mostra o envio e recebimento do pacote de dados entre o cliente DVC e o servidor (plug-in DVC).

![enviando e recebendo um pacote de dados entre o cliente e o servidor do DVC](images/writedvcchannel.png)

 

 




