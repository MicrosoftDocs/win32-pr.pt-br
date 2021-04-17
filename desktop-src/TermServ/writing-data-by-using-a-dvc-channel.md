---
title: Gravando dados usando um canal DVC
description: Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780092"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Gravando dados usando um canal DVC

Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente. A gravação de dados do canal é implementada pelo método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) da interface [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .

A ilustração a seguir mostra o envio e recebimento do pacote de dados entre o cliente DVC e o servidor (plug-in DVC).

![enviando e recebendo um pacote de dados entre o cliente e o servidor do DVC](images/writedvcchannel.png)

 

 




