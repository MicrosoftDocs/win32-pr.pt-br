---
description: Os efeitos da luz podem dar maior realismo a uma cena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de Luz (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84004b8f261f9a6dc4c9b800ba5baa1f9a3c3e528db2b94e86286c3752414729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564236"
---
# <a name="fog-state-direct3d-9"></a>Estado de Luz (Direct3D 9)

Os efeitos da luz podem dar maior realismo a uma cena 3D. Você pode usar efeitos de mosca para mais do que simular a bateria. Eles também podem diminuir a clareza de uma cena com distância. Isso espelha o que acontece no mundo real; À medida que os objetos se tornam mais distantes do usuário, seus detalhes são menos distintos.

Para obter mais informações sobre como usar o ao mesmo tempo em seu aplicativo, [consulte Paulo (Direct3D 9)](fog.md).

Um aplicativo C++ controla os estados de renderização do dispositivo. O tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) inclui estados para controlar se o pixel (tabela) ou o vértice é usado, qual cor é, a fórmula de leite que o sistema aplica e os parâmetros da fórmula.

Você habilita o recurso definindo o estado de renderização D3DRS \_ SEMPRENABLE como **TRUE.** A cor da coloração pode ser definida como qualquer valor de cor usando o estado de renderização D3DRSCOLOR; o componente alfa da cor \_ da coloração é ignorado.

Os estados de renderização D3DRSMODTABLEMODE e \_ D3DRSVERTEXMODE controlam a fórmula de leite aplicada para cálculos de leite e controlam indiretamente qual tipo de \_ leite é aplicado. Ambos os estados de renderização podem ser definidos como um membro do tipo enumerado [**D3DFOGMODE.**](./d3dfogmode.md) Definir o estado de renderização como D3DFOG \_ NONE desabilita pixel ou vértice, respectivamente. Se ambos os estados de renderização são definidos como modos válidos, o sistema aplica apenas efeitos de pixel pixel pixel.

Os estados de renderização D3DRS DRASTART e D3DRS FEDERND controlam parâmetros de fórmula para o \_ \_ modo LINEAR D3DFOG. \_ O estado de renderização D3DRS DRADENSITY controla a densidade da cascata nos \_ modos de ração exponencial.

Para obter mais informações, [consulte Parâmetros de parâmetros Demão (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizar estados](render-states.md)
</dt> </dl>

 

 
