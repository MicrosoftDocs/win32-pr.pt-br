---
title: Visão geral da arquitetura de gráficos do Windows
description: Descreve as APIs de gráficos do C++/COM no Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104091861"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Visão geral da arquitetura de gráficos do Windows

O Windows fornece várias APIs do C++/COM para gráficos. Essas APIs são mostradas no diagrama a seguir.

![um diagrama que mostra as APIs de gráficos do Windows.](images/graphics01.png)

-   Graphics Device Interface (GDI) é a interface gráfica original do Windows. O GDI foi gravado primeiro para Windows de 16 bits e, em seguida, atualizado para o Windows de 32 bits e 64 bits.
-   O GDI+ foi introduzido no Windows XP como um sucessor da GDI. A biblioteca GDI+ é acessada por meio de um conjunto de classes C++ que encapsulam funções Flat C. O .NET Framework também fornece uma versão gerenciada do GDI+ no namespace **System. Drawing** .
-   O Direct3D dá suporte a gráficos 3D.
-   O Direct2D é uma API moderna para gráficos 2D, o sucessor para GDI e GDI+.
-   DirectWrite é um mecanismo de layout e rasterização de texto. Você pode usar GDI ou Direct2D para desenhar o texto rasterizado.
-   O DXGI (infra-estrutura de gráficos do DirectX) executa tarefas de baixo nível, como apresentar quadros para saída. A maioria dos aplicativos não usa DXGI diretamente. Em vez disso, ele serve como uma camada intermediária entre o driver de gráficos e o Direct3D.

Direct2D e DirectWrite foram introduzidos no Windows 7. Eles também estão disponíveis para o Windows Vista e o Windows Server 2008 por meio de uma atualização de plataforma. Para obter mais informações, consulte [atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D é o foco deste módulo. Embora o GDI e o GDI+ continuem a ter suporte no Windows, Direct2D e DirectWrite são recomendados para novos programas. Em alguns casos, uma combinação de tecnologias pode ser mais prática. Para essas situações, Direct2D e DirectWrite são projetados para interoperar com o GDI.

As seções a seguir descrevem alguns dos benefícios do Direct2D.

### <a name="hardware-acceleration"></a>Aceleração de hardware

O termo *aceleração de hardware* refere-se a cálculos de gráficos executados pela GPU (unidade de processamento gráfico), em vez da CPU. As GPUs modernas são altamente otimizadas para os tipos de computação usados na renderização de elementos gráficos. Em geral, quanto mais desse trabalho é movido da CPU para a GPU, melhor.

Embora a GDI dê suporte à aceleração de hardware para determinadas operações, muitas operações de GDI são associadas à CPU. O Direct2D é colocado em camadas sobre o Direct3D e aproveita totalmente a aceleração de hardware fornecida pela GPU. Se a GPU não oferecer suporte aos recursos necessários para o Direct2D, o Direct2D retornará para a renderização de software. De modo geral, o Direct2D supera a GDI e a GDI+ na maioria das situações.

### <a name="transparency-and-anti-aliasing"></a>Transparência e suavização de serrilhado

O Direct2D dá suporte a transparências totalmente aceleradas por hardware.

O GDI tem suporte limitado para a combinação alfa. A maioria das funções GDI não dá suporte à mistura alfa, embora o GDI ofereça suporte à mistura alfa durante uma operação BitBlt. O GDI+ dá suporte à transparência, mas a combinação alfa é executada pela CPU, portanto, não se beneficia da aceleração de hardware.

A combinação de hardware acelerada por alfa também permite suavização de serrilhado. A definição de *alias* é um artefato causado pela amostragem de uma função contínua. Por exemplo, quando uma linha curva é convertida em pixels, o alias pode causar uma aparência irregular. \[ 3 \] qualquer técnica que reduz os artefatos causados por alias é considerada uma forma de suavização de serrilhado. Em gráficos, a suavização de serrilhado é feita por meio da mesclagem de bordas com o plano de fundo. Por exemplo, aqui está um círculo desenhado pela GDI e o mesmo círculo desenhado por Direct2D.

![uma ilustração de técnicas de suavização de alias no Direct2D.](images/graphics02.png)

A imagem a seguir mostra um detalhe de cada círculo.

![um detalhe da imagem anterior.](images/graphics03.png)

O círculo desenhado por GDI (left) consiste em pixels pretos que aproximam uma curva. O círculo desenhado por Direct2D (direita) usa a mesclagem para criar uma curva mais suave.

O GDI não oferece suporte a suavização de serrilhado ao desenhar geometria (linhas e curvas). O GDI pode desenhar texto com suavização de alias usando ClearType; Mas do contrário, o texto GDI também tem um alias. A criação de alias é particularmente perceptível para texto, pois as linhas denteadas interrompem o design da fonte, tornando o texto menos legível. Embora o GDI+ ofereça suporte a suavização de serrilhado, ele é aplicado pela CPU, portanto, o desempenho não é tão bom quanto Direct2D.

### <a name="vector-graphics"></a>Gráficos vetoriais

O Direct2D dá suporte a *gráficos vetoriais*. Em gráficos vetoriais, fórmulas matemáticas são usadas para representar linhas e curvas. Essas fórmulas não dependem da resolução da tela, portanto, podem ser dimensionadas para dimensões arbitrárias. Os gráficos vetoriais são particularmente úteis quando uma imagem deve ser dimensionada para dar suporte a diferentes tamanhos de monitor ou resoluções de tela.

## <a name="next"></a>Avançar

[O Gerenciador de Janelas da Área de Trabalho](the-desktop-window-manager.md)

 

 
