---
title: APIs de gráficos no Windows
description: Este artigo aborda os recursos e as APIs de gráficos do Windows.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366564"
---
# <a name="graphics-apis-in-windows"></a>APIs de gráficos no Windows

O Windows Vista inclui suporte para um modelo de driver de vídeo totalmente novo que representa uma revisão importante no design de drivers de vídeo desde a introdução do Windows Driver Model (WDM) para Windows 98. Esse modelo reprojetado reflete a evolução do hardware de vídeo do mundo das operações de varredura 2D e dos aplicativos GDI para os jogos 3D com hardware de gráficos de funções fixas e, por fim, a partir da GPU (unidade de processamento gráfico) programável moderna que dá suporte a uma ampla gama de aplicativos gráficos de alto desempenho. O Windows 7 e o Windows 8 se baseiam na infraestrutura gráfica do Windows Vista fornecendo recursos gráficos e APIs adicionais. Este artigo aborda os recursos e as APIs de gráficos do Windows.

-   [Tela de fundo](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10,1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11,1](#direct3d-111)
-   [OpenGL](#opengl)
-   [Compatibilidade de aplicativos, GDI e versões mais antigas do Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Recomendações](#recommendations)

## <a name="background"></a>Tela de fundo

A API principal para a programação de gráficos desde o início do Windows é a interface gráfica do dispositivo (GDI). Essa API foi projetada para lidar com vários dispositivos de saída 2D e formou a base para a experiência de interface do usuário do Windows. O DirectDraw e o Direct3D foram introduzidos como APIs alternativas para dar suporte a jogos de tela inteira e renderização 3D como extensões para o hardware existente do tempo. As interações com o GDI eram complicadas. A intermistura efetiva de elementos GDI tradicionais com elementos de Direct3D foi limitada por esse design. A versão do Windows XP do WDM, conhecida como XPDM, reflete a natureza lado a lado do GDI e do Direct3D (consulte a Figura 1).

**Figura 1. APIs de gráficos no Windows XP**

![xpdm](images/graphics-apis-in-windows-xp.gif)

Ao longo dos anos, o poder das placas de vídeo 3D cresceu drasticamente para o ponto em que a grande maioria do hardware é dedicada a essa função. Um novo modelo de driver, o WDDM (Windows Display Driver Model), traz a GPU e o Direct3D para o Forefront, permitindo a criação de uma experiência totalmente nova, a área de trabalho 3D, que combina diretamente o mundo 2D do GDI com o poder das GPUs modernas programáveis. Com o WDDM, o hardware de vídeo é totalmente controlado pelo Direct3D e todas as outras interfaces gráficas se comunicam com o hardware de vídeo por meio do novo modelo de driver centrado em Direct3D (veja a Figura 2).

**Figura 2. APIs de gráficos no Windows Vista**

![compatíveis](images/graphics-apis-in-windows-vista.gif)

Para obter mais informações sobre o WDDM, consulte o [Guia de design do WDDM (Windows Vista Display Driver Model)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) no msdn.

## <a name="direct3d-9"></a>Direct3D 9

A versão 9 do DirectX foi lançada pela primeira vez para Windows no 2002, com atualizações subsequentes no 2003 e 2004. Essa API representa uma década de evolução das tecnologias DirectX, a introdução de modelos de programação de sombreador mais poderosos para Direct3D e uma maturidade apoiada por milhares de títulos de envio. O Direct3D 9 é a principal interface gráfica do Windows Vista. Ele permanece a API ideal a ser usada para escrever jogos e aplicativos 3D que precisam ser executados na ampla gama de versões de hardware e Windows existentes. Os detalhes do novo modelo de driver estão ocultos dos aplicativos que usam as interfaces do Direct3D 9, mas nos bastidores, o sistema operacional está aproveitando totalmente os novos recursos para fornecer uma verdadeira multitarefa de GPU, um gerenciamento de recursos mais eficiente e um desempenho robusto.

Para garantir a compatibilidade total com versões mais antigas do Windows, algumas sutilezas do antigo modelo de driver devem ser emuladas mesmo com o novo modelo de driver de vídeo do Windows Vista. Por exemplo, quando um aplicativo de tela inteira perde o foco, ele deve assumir que perdeu todos os recursos na memória de vídeo (VRAM) e recarregá-los criados como recursos não gerenciados, embora o novo modelo de driver manipule os recursos de forma transparente sem removê-los do contexto do dispositivo. Até mesmo o conceito de um tipo de recurso gerenciado vs. padrão é específico para o antigo modelo de driver. Outro exemplo é a expectativa de falha ao alocar recursos não gerenciados (pool padrão) excedendo a quantidade de VRAM disponível, embora o novo modelo de driver possa fornecer uma quantidade quase ilimitada de memória de vídeo virtual. Devido a esses requisitos, os aplicativos Direct3D em execução no Windows Vista ainda receberão essas condições de erro. Portanto, eles são limitados em sua capacidade de usar as interfaces básicas do Direct3D 9 para usar totalmente alguns recursos do novo modelo de driver.

Enquanto novos sistemas entregues com o Windows Vista incluirão placas de vídeo com drivers WDDM, e novos drivers para várias placas de vídeo populares são incluídos na caixa, o Windows Vista continua a oferecer suporte à capacidade de usar drivers XPDM mais antigos para atualizações e edições corporativas. Em sistemas que usam o antigo modelo de driver, o Direct3D 9 e as interfaces mais antigas devem ser usados, e a operação do sistema de gráficos é muito semelhante à do Windows XP (Figura 1). O WDDM é necessário para que os aplicativos usem o Direct3D 9Ex, o Direct3D 10 e versões posteriores.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

A interface do Direct3D 9Ex fornece acesso a uma pequena extensão da API padrão do Direct3D 9 que expõe a alocação de recursos virtualizados, nova semântica de dispositivo perdido e alguns outros novos recursos disponíveis durante a execução no Windows Vista. Ao criar esse objeto estendido, a API do Direct3D 9 usa a nova semântica e, portanto, requer que o aplicativo use lógica diferente (e, portanto, caminhos de código diferentes) para criação de recursos, gerenciamento e tratamento de erros para novos tipos de condições. Essa API só está disponível no Windows Vista e requer drivers WDDM. Como o Direct3D 9Ex usa uma API e um caminho de código de driver separados do que o Direct3D 9, o suporte a essa API requer casos de teste adicionais para seu aplicativo.

O principal motivo para criar a nova API do Direct3D 9Ex era permitir acesso completo aos novos recursos do WDDM, mantendo, ao mesmo tempo, a compatibilidade para aplicativos Direct3D existentes. A nova área de trabalho 3D e muitos aplicativos específicos do Windows Vista usam esta versão do Direct3D 9, mas não são funcionais quando executados em drivers XPDM mais antigos. Como a API do Direct3D 9Ex nunca aparecerá em versões anteriores do Windows devido à falta de suporte para o WDDM, as interfaces padrão do Direct3D 9 abrangem um conjunto muito mais amplo de sistemas. Para aplicativos de alto desempenho que podem aproveitar a próxima geração de hardware de vídeo, a nova versão 10 do Direct3D fornece muitos recursos novos não expostos pelo Direct3D 9Ex. Como resultado, para jogos e a maioria dos outros aplicativos, o Direct3D 9 ou o Direct3D 10 é a API recomendada.

> [!Note]  
> O SDK do DirectX não fornece amostras, cabeçalhos ou bibliotecas para a interface do Direct3D 9Ex. A biblioteca MSDN e o SDK do Windows (anteriormente conhecido como Platform SDK) contêm a documentação, os cabeçalhos e as bibliotecas disponíveis.

 

Para obter mais informações sobre o Direct3D 9Ex, consulte [DirectX para Windows Vista](/previous-versions//ms681824(v=vs.85)) em msdn.

## <a name="direct3d-10"></a>Direct3D 10

Para obter completamente o potencial do novo modelo de driver do Windows Vista e de hardware de última geração, uma versão totalmente nova da API do Direct3D foi criada. Embora o WDDM elimine algumas das limitações no desempenho do sistema gráfico existente, o Direct3D 10 vai além, removendo os afunilamentos de design na API do Direct3D existente e simplifica muito a tarefa de programação da GPU.

A nova API elimina completamente todos os aspectos de funções fixas, substituindo-os por construções programáveis e simplificando muito a implementação interna. Os centenas de bits de recursos em versões anteriores do Direct3D foram completamente eliminados e substituídos por um conjunto de funcionalidades bem definido e inclusivo que tem apenas alguns cenários de uso opcionais para formatos de recursos específicos. A criação e a validação de recursos com uso intensivo de CPU agora têm semântica explícita na nova API. Isso permite um comportamento de desempenho muito mais previsível e reduz a sobrecarga por empate. Os recursos podem ser reconfigurados em vários formulários para permitir o uso eficiente em vários estágios, e o conjunto de recursos impõe muito menos restrições em cenários de uso para formatos. Há também novos formatos de textura de mapa normal compactados em bloco.

Na nova API, as constantes do sombreador e o estado do dispositivo são recursos explícitos, permitindo um cache muito mais eficiente no hardware e uma validação de driver muito simplificada. O modelo de sombreador programável foi unificado entre os sombreadores de vértice e de pixel e tornou-se mais expressivo com um modelo computacional e um conjunto de operadores bem definidos. Além disso, um novo estágio Geometry Shader foi adicionado para operar em primitivos após o estágio do sombreador de vértice. Os resultados do trabalho da GPU no vértice e nos estágios do sombreador de geometria do pipeline podem ser transmitidos para a RAM de vídeo para reutilização, permitindo a possibilidade de operações de GPU de várias passagens extremamente complexas com interação mínima de CPU.

Todos esses aprimoramentos permitem a tecnologia gráfica de última geração e ampliam a capacidade dos aplicativos de trabalhar fora de carga para a GPU. O descarregamento permite uma aparência de caracteres mais complexa baseada em GPU, técnicas de metamorfose aceleradas, geração de volume de sombra e extrusão, partículas e sistemas de física que são totalmente baseados em GPU, materiais mais complexos combinados em lotes eficientes de desenho grande, detalhes de procedimentos, mapeamento de deslocamento de Ray-Traced em tempo real, geração de mapa de cubos de passagem única e muito mais técnicas – tudo isso ao mesmo tempo que libera recursos de CPU para aplicativos mais

Para fornecer esse nível de inovação no Direct3D 10, o hardware mais antigo não pode ser expresso como uma implementação parcial de uma nova interface. Uma placa de vídeo é capaz de dar suporte a todos os novos recursos ou não é um cartão com capacidade para Direct3D 10. Portanto, embora o Direct3D 9 pudesse impulsionar o hardware DirectX7 com muitos bits de capacidade e limitações de uso ausentes, o Direct3D 10 funciona apenas em uma nova geração de placas de vídeo. Para que um aplicativo ofereça suporte a hardware de vídeo mais antigo, ele também deve oferecer suporte às interfaces do Direct3D 9. Versões futuras do Direct3D serão criadas na versão 10, estendendo-as para novas versões da API, garantindo um superconjunto estrito de funcionalidade do Direct3D 10.

Para obter mais informações sobre o Direct3D 10, consulte [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10,1

O Windows Vista Service Pack 1 estende a API do Direct3D 10 com o Direct3D 10,1, que adiciona interfaces opcionais e um modelo de sombreador adicional para dar suporte a novos recursos de hardware de placas de vídeo que dão suporte ao Direct3D 10,1. Todo o hardware que é capaz de dar suporte ao Direct3D 10,1 também dá suporte completo a todos os recursos do Direct3D 10, e os desenvolvedores de jogos podem usar os recursos adicionais do Direct3D 10,1, quando disponíveis.

> [!Note]  
> O Direct3D 10,1 é a API de gráficos usada pela área de trabalho do Windows 7.

 

> [!Note]  
> O Windows 7 e a atualização do Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) adicionam suporte para dxgi 1,1, níveis de recursos 10level9 e o dispositivo WARP10 para a API do Direct3D 10,1 existente.

 

## <a name="direct3d-11"></a>Direct3D 11

O Windows 7 dá suporte a uma nova revisão do Direct3D, Direct3D 11, criada com base no design da API do Direct3D 10,1. Os novos recursos da API incluem processamento multithread e criação de recursos, sombreador de computação, suporte para níveis de recursos 10level9 e o dispositivo de renderização de software WARP10 e novos recursos de hardware de classe Direct3D 11, como mosaico usando envoltória & sombreadores de domínio, BC6H e BC7 formatos de compactação de textura, modelo de sombreador 5,0 e vinculação de sombreador dinâmico. A nova API pode usar placas de vídeo de classe Direct3D 10 e 10,1 existentes, algumas placas Direct3D 9 por meio dos níveis de recurso 10level9 com suporte limitado a recursos e a última geração de placas de vídeo de classe Direct3D 11.

Além da API do Direct3D 11, o Windows 7 inclui DXGI 1,1, Direct2D, DirectWrite e suporte para drivers WDDM 1,1.

> [!Note]  
> O Direct3D 11 e as APIs relacionadas também estão disponíveis como uma atualização para o Windows Vista (consulte [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11,1

O Windows 8 estende a [API do Direct3D 11](#direct3d-11) com o Direct3D 11,1. O Direct3D 11,1 dá suporte a todos os hardwares existentes que oferecem suporte aos [níveis de recursos](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11, 10 \_ x e 9 \_ x, bem como um novo nível de recurso de 11 \_ 1.

Além da API do [Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features), o Windows 8 inclui o [dxgi 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [contextos de dispositivo Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts)e suporte para drivers do WDDM 1,2.

> [!Note]  
> Se você quiser que seus aplicativos da Windows Store programem gráficos 3D com o DirectX, você poderá usar a API do Direct3D 11,1. Para obter mais informações sobre como programar gráficos 3D com o DirectX, consulte [introdução aos gráficos 3D com DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).

 

**Atualização de plataforma para o Windows 7:** O suporte parcial está disponível para a [API do Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) no Windows 7 ou no windows Server 2008 R2 com a [atualização da plataforma para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obter mais informações sobre a atualização de plataforma para o Windows 7, consulte [atualização de plataforma para Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>OpenGL

O Windows Vista, o Windows 7 e o Windows 8 fornecem o mesmo suporte que o Windows XP para OpenGL, que permite que os fabricantes de placas de vídeo forneçam um driver de cliente instalável (ICD) para OpenGL que fornece suporte acelerado por hardware. Observe que as versões mais recentes de tais ICDs são necessárias para oferecer suporte total ao Windows Vista, ao Windows 7 ou ao Windows 8. Se nenhum ICD estiver instalado, o sistema fará fallback para a camada de software OpenGL v 1.1 na maioria dos casos.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilidade de aplicativos, GDI e versões mais antigas do Direct3D

Os sistemas de gráficos do Windows Vista, do Windows 7 e do Windows 8 foram projetados para dar suporte a uma ampla gama de cenários de uso e hardware para permitir novas tecnologias enquanto continuam a oferecer suporte a sistemas existentes. As interfaces gráficas existentes, como GDI, GDI+ e versões mais antigas do Direct3D, continuam funcionando no Windows Vista e no Windows 7, mas são remapeadas internamente sempre que possível. Isso significa que a maioria dos aplicativos existentes do Windows continuará a funcionar.

O Windows Vista, o Windows 7 e o Windows 8 continuam a dar suporte às mesmas interfaces Direct3D e DirectDraw que o Windows XP, de volta à versão 3 do DirectX (com exceção do modo retido Direct3D's, que foi removido). Assim como acontece com o Windows XP Professional x64 Edition, os aplicativos nativos de 64 bits nas versões mais recentes do Windows são limitados a Direct3D9, DirectDraw7 ou interfaces mais recentes. Aplicativos de alto desempenho devem usar o Direct3D 9 ou posterior para garantir que eles tenham a correspondência mais próxima com os recursos de hardware.

## <a name="recommendations"></a>Recomendações

Considere as seguintes recomendações ao selecionar uma API para seu aplicativo gráfico:

-   Use o Direct3D 9 se seu aplicativo precisar oferecer suporte ao Windows XP ou a uma versão anterior do Windows.
-   Use o Direct3D 9 se você quiser dar suporte ao Windows Vista ou ao Windows 7 em execução com drivers XPDM. Para sistemas Windows Vista ou Windows 7 que não têm um hardware de vídeo Direct3D 10 ou melhor, você pode optar por usar o caminho de código do Windows XP Direct3D 9 existente ou usar os níveis de recurso 10level9 por meio da API Direct3D 10,1 ou Direct3D 11.
-   Use o Direct3D 11 para aproveitar a próxima geração de hardware de vídeo no Windows Vista, no Windows 7 e no Windows 8. Os aplicativos da Windows Store devem usar o Direct3D 11 ou posterior.

 

 