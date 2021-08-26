---
description: A animação de paleta é uma técnica para simular o movimento alterando rapidamente as cores das entradas selecionadas em uma paleta de cores.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animação da paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ea2d557ddd071a8f8e993f3a797fb42c2f4fef9abc68fc13737cded96a18fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965586"
---
# <a name="palette-animation"></a>Animação da paleta

A animação de paleta é uma técnica para simular o movimento alterando rapidamente as cores das entradas selecionadas em uma paleta de cores. Um aplicativo pode executar a animação da paleta criando uma paleta lógica que contém entradas "reservadas" e, em seguida, usando a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar as cores nessas entradas reservadas.

Um aplicativo cria uma entrada reservada em uma paleta lógica definindo o membro **peFlags** da estrutura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) para o \_ sinalizador reservado para PC. Depois que essa paleta lógica é selecionada e realizada, o aplicativo pode chamar a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar uma ou mais entradas reservadas. Se a paleta fornecida estiver associada à janela ativa, o sistema atualizará as cores na tela imediatamente.

 

 
