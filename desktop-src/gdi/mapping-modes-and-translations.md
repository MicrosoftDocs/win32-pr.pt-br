---
description: Os modos de mapeamento são descritos na tabela a seguir.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modos de mapeamento e traduções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219bfe2f587ef9bc66f53d6f08404a0448180512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165069"
---
# <a name="mapping-modes-and-translations"></a>Modos de mapeamento e traduções

Os modos de mapeamento são descritos na tabela a seguir.



| Modo de mapeamento    | Description                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ANISOTROPIC mm | Cada unidade no espaço de página é mapeada para uma unidade especificada pelo aplicativo no espaço do dispositivo. O eixo pode ou não ser dimensionado igualmente (por exemplo, um círculo desenhado no espaço de mundo pode parecer ser uma elipse quando representado em um determinado dispositivo). A orientação do eixo também é especificada pelo aplicativo.                  |
| \_HIENGLISH mm   | Cada unidade no espaço de página é mapeada para 0, 1 polegadas no espaço do dispositivo. O valor de x aumenta da esquerda para a direita. O valor de y aumenta de baixo para cima.                                                                                                                                                                 |
| \_HIMETRIC mm    | Cada unidade no espaço de página é mapeada para 0, 1 milímetros no espaço do dispositivo. O valor de x aumenta da esquerda para a direita. O valor de y aumenta de baixo para cima.                                                                                                                                                            |
| \_ISOTROPIC mm   | Cada unidade no espaço de página é mapeada para uma unidade definida pelo aplicativo no espaço do dispositivo. Os eixos são sempre igualmente dimensionados. A orientação dos eixos pode ser especificada pelo aplicativo.                                                                                                                                     |
| \_LOENGLISH mm   | Cada unidade no espaço de página é mapeada para 0, 1 polegadas no espaço do dispositivo. O valor de x aumenta da esquerda para a direita. O valor de y aumenta de baixo para cima.                                                                                                                                                                  |
| \_LOMETRIC mm    | Cada unidade no espaço de página é mapeada para 0,1 milímetros no espaço do dispositivo. O valor de x aumenta da esquerda para a direita. O valor de y aumenta de baixo para cima.                                                                                                                                                             |
| \_texto mm        | Cada unidade no espaço de página é mapeada para um pixel; ou seja, nenhum dimensionamento é realizado. Quando nenhuma tradução está em vigor (esse é o padrão), o espaço de página no \_ modo de mapeamento de texto mm é equivalente ao espaço físico do dispositivo. O valor de x aumenta da esquerda para a direita. O valor de y aumenta de cima para baixo. |
| \_TWIPS mm       | Cada unidade no espaço de página é mapeada para um vigésimo do ponto de uma impressora (1/1440 polegada). O valor de x aumenta da esquerda para a direita. O valor de y aumenta de baixo para cima.                                                                                                                                           |



 

Para definir um modo de mapeamento, chame a função [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Recupere o modo de mapeamento atual para um controlador de domínio chamando a função [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) .

As transformações de espaço de página para dispositivo-espaço consistem em valores calculados dos pontos fornecidos pela janela e pelo visor. Nesse contexto, a janela refere-se ao sistema lógico de coordenadas do espaço da página, enquanto o visor refere-se ao sistema de coordenadas do dispositivo do espaço do dispositivo. A janela e o visor consistem em uma origem, uma extensão horizontal ("x") e uma extensão vertical ("y"). Os parâmetros da janela estão em coordenadas lógicas; o visor nas coordenadas do dispositivo (pixels). O sistema combina as origens e extensões da janela e do visor para criar a transformação. Isso significa que a janela e o visor especificam a metade dos fatores necessários para definir a transformação usada para mapear pontos no espaço da página para o espaço do dispositivo. Assim, o sistema mapeia a origem da janela para a origem do visor e as extensões da janela para as extensões do visor, conforme mostrado na ilustração a seguir.

![ilustração mostrando uma origem de janela em espaço de página e uma origem de ponto de vista no espaço do dispositivo](images/cstrn-15.png)

As extensões Window e viewport estabelecem uma proporção ou fator de dimensionamento usado no espaço de página para transformações de espaço em dispositivo. Para os seis modos de mapeamento predefinidos (MM \_ HIENGLISH, mm \_ LOENGLISH, mm \_ HIMETRIC, mm \_ LOMETRIC, \_ texto mm e mm \_ TWIPS), as extensões são definidas pelo sistema quando [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) é chamado. Eles não podem ser alterados. Os outros dois modos de mapeamento (MM \_ ISOTROPIC e mm \_ ANISOTROPIC) exigem que as extensões sejam especificadas. Isso é feito chamando **SetMapMode** para definir o modo apropriado e, em seguida, chamar as funções [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) e [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) para especificar as extensões. No modo de \_ mapeamento mm ISOTROPIC, é importante chamar **SetWindowExtEx** antes de chamar **SetViewportExtEx**.

As origens de janela e visor estabelecem a tradução usada no espaço de página para transformações de espaço de dispositivo. Defina as origens da janela e do visor usando as funções [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) e [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . As origens são independentes das extensões e um aplicativo pode defini-las independentemente do modo de mapeamento atual. A alteração de um modo de mapeamento não afeta as origens definidas no momento (embora possa afetar as extensões). As origens são especificadas em unidades absolutas que o modo de mapeamento atual não afeta. Para alterar as origens, use as funções [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) e [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) .

A fórmula a seguir mostra a matemática envolvida na conversão de um ponto do espaço de página para o espaço do dispositivo.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

As variáveis a seguir estão envolvidas.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

A mesma equação com y substituindo x transforma o y componentof em um ponto.

A fórmula primeiro desloca o ponto de sua origem de coordenadas. Esse valor, que não é mais tendenciosa pela origem, é então dimensionado para o sistema de coordenadas de destino pela proporção das extensões. Por fim, o valor escalado é deslocado pela origem de destino para seu mapeamento final.

As funções [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) e [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) podem ser usadas para converter de pontos lógicos em pontos de dispositivo e de pontos de dispositivo em pontos lógicos, respectivamente.

 

 



