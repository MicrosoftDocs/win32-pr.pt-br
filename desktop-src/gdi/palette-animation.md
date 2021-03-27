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
# <a name="palette-animation"></a><span data-ttu-id="c4bac-103">Animação da paleta</span><span class="sxs-lookup"><span data-stu-id="c4bac-103">Palette Animation</span></span>

<span data-ttu-id="c4bac-104">A animação de paleta é uma técnica para simular o movimento alterando rapidamente as cores das entradas selecionadas em uma paleta de cores.</span><span class="sxs-lookup"><span data-stu-id="c4bac-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="c4bac-105">Um aplicativo pode executar a animação da paleta criando uma paleta lógica que contém entradas "reservadas" e, em seguida, usando a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar as cores nessas entradas reservadas.</span><span class="sxs-lookup"><span data-stu-id="c4bac-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="c4bac-106">Um aplicativo cria uma entrada reservada em uma paleta lógica definindo o membro **peFlags** da estrutura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) para o \_ sinalizador reservado para PC.</span><span class="sxs-lookup"><span data-stu-id="c4bac-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="c4bac-107">Depois que essa paleta lógica é selecionada e realizada, o aplicativo pode chamar a função [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) para alterar uma ou mais entradas reservadas.</span><span class="sxs-lookup"><span data-stu-id="c4bac-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="c4bac-108">Se a paleta fornecida estiver associada à janela ativa, o sistema atualizará as cores na tela imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c4bac-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
