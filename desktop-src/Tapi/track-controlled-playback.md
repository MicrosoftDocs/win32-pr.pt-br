---
description: As etapas a seguir são executadas para a reprodução controlada por controle.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Reprodução de Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc26cd1448c712b99a0e61bf94520531c1c592a289d273257c8bc907b266eea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002614"
---
# <a name="track-controlled-playback"></a>Reprodução de Track-Controlled

Para executar a reprodução controlada pelo controle, faça o seguinte:

-   Selecione a faixa terminais em fluxos.
-   Crie o terminal de reprodução de arquivo.
-   Definir propriedades — nome do arquivo e tipo de armazenamento.
-   Usando um método no terminal de reprodução de arquivo, enumere os terminais de faixa de arquivo.
-   Enumere os fluxos na chamada TAPI.
-   Selecione o terminal de faixa de arquivo no fluxo.
-   Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de reprodução de arquivos para iniciar a reprodução de dados gravados nos fluxos TAPI.

 

 



