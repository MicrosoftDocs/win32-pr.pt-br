---
description: Os terminais de arquivo podem ser usados de duas maneiras.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Usando terminais de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091759"
---
# <a name="using-file-terminals"></a>Usando terminais de arquivo

Os terminais de arquivo podem ser usados de duas maneiras. O método mais simples é usar [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) para selecionar um terminal de arquivo (reprodução ou registro) em um objeto de chamada TAPI. Nesse caso, a TAPI cuida da conexão dos fluxos de áudio aos terminais de faixa.

O segundo método permite que um aplicativo tenha um controle mais preciso sobre o mapeamento de fluxos de áudio para faixas. Nesse cenário, o aplicativo enumera os fluxos disponíveis na chamada, escolhe aqueles que deseja registrar (ou use para reprodução), cria (ou localiza para reprodução) as faixas correspondentes no terminal do arquivo e seleciona as faixas em fluxos de chamada.

Para mais informações, consulte os seguintes tópicos:

-   [Reprodução simples](simple-playback.md)
-   [Controle de reprodução controlado](track-controlled-playback.md)
-   [Registro simples](simple-record.md)
-   [Rastrear registro controlado](track-controlled-record.md)

 

 



