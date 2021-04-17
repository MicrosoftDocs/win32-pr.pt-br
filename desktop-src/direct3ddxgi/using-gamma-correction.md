---
description: A correção gama, ou gama, para curto, é o nome de uma operação não linear que os sistemas usam para codificar e decodificar valores de pixel em imagens.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Usando a correção gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c940db1a94fb41e9babecbeb3075aa9e01b3732
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566479"
---
# <a name="using-gamma-correction"></a>Usando a correção gama

A correção gama, ou gama, para curto, é o nome de uma operação não linear que os sistemas usam para codificar e decodificar valores de pixel em imagens.

-   [O que é o gama e para que se trata?](#what-is-gamma-and-what-is-it-for)
-   [Plano de fundo de gama no Windows](#background-of-gamma-on-windows)
-   [Evolução do hardware de vídeo](#evolution-of-display-hardware)
-   [Recursos de controle de gama em DXGI](#gamma-control-capabilities-in-dxgi)
-   [Definindo o controle gama com DXGI](#setting-gamma-control-with-dxgi)
-   [Práticas de controle de gama](#gamma-control-practicalities)
-   [Tópicos relacionados](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>O que é o gama e para que se trata?

No final do pipeline de gráficos, apenas onde a imagem deixa o computador para fazer sua jornada ao longo do cabo do monitor, há uma pequena parte do hardware que pode transformar valores de pixel em tempo real. Esse hardware geralmente usa uma tabela de pesquisa para transformar os pixels. Esse hardware usa os valores vermelho, verde e azul provenientes da superfície a ser exibida para pesquisar valores corrigidos em gama na tabela e, em seguida, envia os valores corrigidos para o monitor em vez dos valores reais da superfície. Portanto, essa tabela de pesquisa é uma oportunidade de substituir qualquer cor por qualquer outra cor. Embora a tabela tenha esse nível de potência, o uso típico é ajustar as imagens sutilmente para compensar as diferenças na resposta do monitor. A resposta do monitor é a função que relaciona o valor numérico dos componentes vermelho, verde e azul de um pixel com o brilho exibido desse pixel.

É para isso que essa tabela se destina, mas os desenvolvedores de jogos encontraram usos criativos para ele, como piscar toda a tela em vermelho para o efeito psicológica. Em aplicativos de jogos modernos, como parte do pós-processamento de cada quadro, normalmente fornecemos outras maneiras de fazer essas coisas. Na verdade, é recomendável deixar a tabela gama sozinha porque ela pode estar em uso para calibrar a resposta do monitor, e as alterações no atacado para a rampa de gama destruirão essa calibragem cuidadosa.

A ciência de determinar a correção de gama é complexa e não é apresentada aqui, além de não se acender de onde veio o nome "gama". Uma resposta do monitor CRT (ou seja, uma velha) é uma função complexa, mas a física desses monitores significa que eles exibem uma resposta que pode ser representada de forma bruta por essa função de energia:

brilho (entrada) =<sup>gama</sup> de entrada

O valor de gama normalmente é próximo ao valor de 2,0. Os monitores LCD e todas as outras tecnologias mais recentes são especificamente desenvolvidos para exibir uma resposta semelhante para que todos os nossos softwares e imagens não precisem ser recalibrados para essas novas tecnologias. O padrão sRGB declara que esse valor de gama é exatamente 2,2, e esse valor se tornou um padrão amplamente implementado.

O olho humano também tem uma função de resposta que aproximadamente inverte a função de energia CRT. Isso significa que o brilho percebido de um pixel aumenta aproximadamente de forma linear com os valores RGB nesse pixel.

Como um valor de gama de 2,2 se tornou um padrão de fato, não precisamos nos preocupar muito com a curva gama codificada nesta tabela e pode deixá-la como um mapeamento linear de um para um. É claro que a correspondência de cores adequada não exige Exquisite com essa função, mas essa discussão está além do escopo deste tópico. O Windows inclui uma ferramenta que permite aos usuários calibrar seus monitores para o gama 2,2, e essa ferramenta usa o hardware da tabela de pesquisa para derivar um ajuste sutil cuidadosamente escolhido para seus computadores. Os usuários podem executar essa ferramenta pesquisando "calibrar cor". Também há perfis de cores bem definidos para monitores específicos que automatizam esse processo. A ferramenta "calibrar cor" pode detectar esses monitores mais recentes e informar aos usuários que a calibragem já está em vigor.

Essa noção de codificar uma lei de energia em valores de cor também é útil em outro lugar no pipeline de gráficos, especialmente em texturas. Para texturas, você quer mais precisão em cores mais escuras devido à resposta de olho humano logarítmica sobre a qual acabamos de falar. Um tratamento cuidadoso de gama nesta parte do pipeline é importante. Para obter mais informações, consulte [convertendo dados para o espaço de cores](converting-data-color-space.md).

O restante deste tópico se concentra apenas na correção gama nesta última parte do pipeline, entre os dados do buffer do quadro e o monitor. Se você quiser escrever um assistente de calibragem ou criar efeitos especiais em um aplicativo de tela inteira em que uma etapa de pós-processamento não é prática, aqui estão as informações necessárias.

## <a name="background-of-gamma-on-windows"></a>Plano de fundo de gama no Windows

Os computadores com Windows normalmente têm uma tabela gama que é uma tabela de pesquisa que usa um terceto de bytes e gera um terceto de bytes. Esses tercetos são 768 (256 x 3) bytes de RAM. Isso é bom quando o formato de exibição contém um terceto de valores de bytes RGB, mas não é expressivo o suficiente para descrever as transformações que você pode querer quando o formato de exibição tem um intervalo maior que \[ 0, 1 \] , como valores de ponto flutuante. As APIs no Windows que controlam o gama seguiram uma evolução à medida que os formatos de exibição se tornaram mais complexos.

As primeiras APIs do Windows para oferecer controle de gama são [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) e [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)da GDI (Windows Graphics Device Interface). Essas APIs funcionam com matrizes de entrada de 3 256 de palavras, com cada palavra codificando zero para uma, representada pelos valores de palavra 0 e 65535. A precisão extra de uma palavra normalmente não está disponível em tabelas de pesquisa de hardware reais, mas essas APIs foram destinadas a serem flexíveis. Essas APIs, em contraste com as outras descritas posteriormente nesta seção, permitem apenas um pequeno desvio de uma função de identidade. Na verdade, qualquer entrada na rampa deve estar dentro de 32768 do valor de identidade. Essa restrição significa que nenhum aplicativo pode ativar a exibição completamente preta ou para outra cor ilegível.

A próxima API é o [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)do Microsoft Direct3D 9, que segue o mesmo padrão e formato de dados que [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp). O valor padrão da rampa de gama de Direct3D 9 não é particularmente útil; é um rampa de palavras inicializado para 0-255, não 0-65535, mesmo que a API seja definida em termos de 0-65535.

A API mais recente é [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Essa API tem um esquema mais flexível para expressar o controle de gama, como se ajusta ao conjunto de formatos de exibição de DXGI, incluindo dez bits de inteiros por canal, formatos float de 16 bits e o \_ formato de intervalo estendido de polarização de XR.

Todas essas APIs operam no mesmo hardware e alteram os mesmos valores. As APIs do Direct3D 9 e DXGI são "somente gravação". Você não pode ler o valor do hardware, modificá-lo e, em seguida, defini-lo. Você só pode definir a rampa. Além disso, você só pode definir o gama quando o aplicativo está em tela inteira. Essa restrição é outra maneira de garantir que a área de trabalho sempre seja legível. Ou seja, o aplicativo pode incomodar sua própria exibição, mas o Windows irá restaurar a rampa de gama anterior quando o aplicativo perde a tela inteira (por exemplo, por meio de Alt-Tab ou Ctrl-Alt-Del).

## <a name="evolution-of-display-hardware"></a>Evolução do hardware de vídeo

Alguns monitores mais recentes podem exibir uma ampla gama de intensidades. Mas, quando o formato de exibição pode representar apenas valores entre zero e um, a exibição deve mapear zero para seu valor mais escuro e um para seu valor mais brilhante. Esse valor mais brilhante pode ser muito claro para a exibição confortável de páginas da Web com texto preto em um plano de fundo branco, mas é maravilhoso para efeitos especiais mais brilhantes, como a exibição do Glittering de luz solar de um lago ou relâmpago de bifurcação do céu. Portanto, precisamos de uma maneira de expressar esses intervalos mais amplos. DXGI 1,1 e posterior contém valores de formato de exibição que permitem que 1,0 representem um valor branco confortável e reservam valores de formato de exibição mais largos para efeitos especiais mais brilhantes. DXGI 1,1 dá suporte a dois formatos de exibição que podem expressar esses valores mais largos: \_ formato dxgi \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM e ponto flutuante de 16 bits. Para obter uma discussão completa sobre esses formatos, consulte [detalhes do formato estendido](/windows-hardware/drivers/display/details-of-the-extended-format). Em seguida, examinamos por que a API gama [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) do dxgi precisa de valores de pixel maiores que 1,0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Recursos de controle de gama em DXGI

DXGI permite que o driver de vídeo Expresse seus controles gama como uma função linear de etapa. Essa função linear por etapa é definida pelos pontos de controle dessa função, o intervalo de valores para os quais a função pode ser convertida e uma operação adicional de escala e deslocamento opcional que pode ser aplicada após a conversão. Um aplicativo pode chamar o método [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para recuperar todos esses recursos de controle na estrutura [**de \_ \_ \_ recursos de controle do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) .

Esse grafo mostra uma função linear com apenas quatro pontos de controle.

![função linear de correção gama](images/gamma-linear-function.png)

DXGI define os pontos de controle por sua localização ao longo do eixo de cores da superfície. No grafo anterior, os locais dos pontos de controle são 0, 0,5, 0,75 e 1,0. Esses pontos de controle indicam que o hardware pode converter valores no intervalo de 0 a 1,0. DXGI lista esses pontos de controle no  membro da matriz ControlPointPositions [**de \_ \_ \_ recursos de controle do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) e sempre os declara em ordem crescente. DXGI preenche apenas os primeiros elementos da matriz **ControlPointPositions** e indica o número de elementos com o membro **NumGammaControlPoints** dos **recursos de \_ \_ controle \_ do dxgi gama**. Se **NumGammaControlPoints** for menor que 1025, DXGI deixará o restante dos elementos **ControlPointPositions** indefinidos.

O hardware representado por esse grafo pode converter valores em um intervalo de 0 a 1,25. Portanto, DXGI define os membros **MinConvertedValue** e **MaxConvertedValue** como 0,0 f e 1,25 f, respectivamente.

DXGI define o membro **ScaleAndOffsetSupported** dos [**\_ \_ \_ recursos de controle do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) para indicar se o hardware dá suporte ao recurso de escala e deslocamento. Se o hardware oferecer suporte a escala e deslocamento, ele mantém uma tabela simples de pesquisa um-para-um, mas, em seguida, ajusta a saída da tabela para alongar a saída para um intervalo maior que \[ 0, 1 \] . O hardware primeiro dimensiona os valores que vêm da tabela de pesquisa e os desloca.

> [!Note]  
> Monitores diferentes conectados ao mesmo computador podem ter diferentes recursos de controle gama. Além disso, os recursos de controle do gama podem, na verdade, mudar dependendo do modo de exibição da saída. Consequentemente, recomendamos que você sempre chame [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) para consultar os recursos de controle de gama depois que seu aplicativo entrar no modo de tela inteira.

 

Você pode usar esses valores de capacidade de controle de gama para derivar valores de controle que podem ser definidos usando a API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

## <a name="setting-gamma-control-with-dxgi"></a>Definindo o controle gama com DXGI

Para definir controles gama, você passa um ponteiro para uma estrutura de [**\_ \_ controle do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) quando chama a API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

Você define os membros de **escala** e **deslocamento** do [**controle de \_ gama \_ de dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) para especificar os valores de escala e deslocamento que você deseja que o hardware aplique aos valores obtidos da tabela de pesquisa. Você pode definir com segurança a **escala** como 1 e o **deslocamento** para zero (ou seja, uma escala por um não tem nenhum efeito e um deslocamento de zero não tem nenhum efeito) se você não quiser usar o recurso de escala e deslocamento ou se o hardware não tiver esse recurso.

Você define o  membro da matriz GammaCurve [**do \_ \_ controle de gama de dxgi**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) para uma lista de estruturas de [**\_ RGB de dxgi**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) para os pontos na curva gama. Cada elemento do **dxgi \_ RGB** especifica os valores float que representam os componentes vermelho, verde e azul para esse ponto. A curva gama não usa valores Alfa. Você usa o número obtido do **NumGammaControlPoints** de recursos de [**\_ \_ controle \_ do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) para preencher esse número de elementos na matriz **GammaCurve** . Cada elemento que você coloca na matriz **GammaCurve** é a altura de cada ponto de controle.

Observe no grafo anterior que agora você tem controle sobre o posicionamento vertical de cada ponto de controle e tem um controle separado para vermelho, verde e azul. Por exemplo, você pode definir todos os valores verdes e azuis como zero e definir os valores vermelhos como uma escada crescente de zero para um. Nesse cenário, a imagem exibida mostra apenas suas partes vermelhas, com azul e verde aparecendo como preto. Você também pode definir uma escada decrescente para todas as cores, o que resulta em uma exibição invertida. Qualquer valor que você coloca na matriz **GammaCurve** deve estar inclusivamente dentro dos valores obtidos dos membros **MinConvertedValue** e **MaxConvertedValue** dos recursos de [**\_ \_ controle \_ do dxgi gama**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Práticas de controle de gama

Os controles de gama de DXGI aplicam-se somente enquanto o aplicativo estiver em tela inteira. O Windows restaura o estado anterior da exibição quando o aplicativo é encerrado ou retorna ao modo de janela. Mas o Windows não restaura o estado de gama do aplicativo se o aplicativo inserir novamente o modo de tela inteira. Seu aplicativo deve restaurar explicitamente seu estado de gama quando ele reinserir o modo de tela inteira.

Nem todos os adaptadores dão suporte ao controle gama. Se um adaptador não oferecer suporte ao controle gama, ele ignorará as chamadas para definir uma rampa de gama.

Os aplicativos executados na área de trabalho remota não podem controlar o gama.

O cursor do mouse, se for implementado em hardware (como a maioria deles), normalmente não responderá à configuração gama.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
