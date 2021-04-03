---
title: O volume escalar
description: O volume escalar
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- MIDI (interface digital de instrumento musical), volume escalar
- MIDI (interface digital de instrumentos musicais), volume escalar
- Mapeador de MIDI, volume escalar
- escalar volume
- Mapeador de MIDI, ajustando os níveis de saída
- ajustando os níveis de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006177"
---
# <a name="the-volume-scalar"></a>O volume escalar

A finalidade do volume escalar é permitir ajustes entre os níveis de saída relativos de patches diferentes em um sintetizador. Por exemplo, se o patch de baixo em um sintetizador estiver muito alto em comparação com seu patch de piano, você poderá alterar o mapa da instalação para reduzir verticalmente o volume de baixo ou o volume de piano.

O volume escalar especifica um valor percentual para alterar todas as mensagens do controlador de volume principal MIDI que seguem uma mensagem de alteração de programa associada. Por exemplo, se o valor escalar do volume for 50%, o mapeador de MIDI modificará as mensagens do controlador de volume de MIDI principal, conforme mostrado na ilustração a seguir.

![imagem do Mapeador MIDI](images/mmap-a04.gif)

 

 




