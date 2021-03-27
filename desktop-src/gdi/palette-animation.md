---
description: A animação de paleta é uma técnica para simular o movimento alterando rapidamente as cores das entradas selecionadas em uma paleta de cores.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animação da paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661591"
---
# <a name="palette-animation"></a>Animação da paleta

A animação de paleta é uma técnica para simular o movimento alterando rapidamente as cores das entradas selecionadas em uma paleta de cores. Um aplicativo pode executar a animação da paleta criando uma paleta lógica que contém entradas "reservadas" e, em seguida, usando a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar as cores nessas entradas reservadas.

Um aplicativo cria uma entrada reservada em uma paleta lógica definindo o membro **peFlags** da estrutura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) para o \_ sinalizador reservado para PC. Depois que essa paleta lógica é selecionada e realizada, o aplicativo pode chamar a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar uma ou mais entradas reservadas. Se a paleta fornecida estiver associada à janela ativa, o sistema atualizará as cores na tela imediatamente.

 

 
