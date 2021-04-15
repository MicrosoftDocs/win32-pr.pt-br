---
title: Especificando recursos de imagem da faixa de uma
description: Como um sistema de apresentação de comando avançado, o Windows Ribbon Framework foi projetado para dar suporte extensivo a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas. Todos os recursos de imagem são declarados na marcação da faixa de lista ou consultados de um aplicativo host da faixa de Ribbon.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Faixa de, recursos de imagem do Windows
- Faixa de das, recursos de imagem
- Faixa de, transparência do Windows
- Faixa de, transparência
- Faixa de, profundidade de cor do Windows
- Faixa de, profundidade de cor
- Faixa de medida do Windows, contraste
- Faixa de faixas, contraste
- recursos de imagem no Windows Ribbon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454266"
---
# <a name="specifying-ribbon-image-resources"></a>Especificando recursos de imagem da faixa de uma

Como um sistema de apresentação de comando avançado, o Windows Ribbon Framework foi projetado para dar suporte extensivo a recursos de imagem em toda a interface do usuário (IU) da faixa de faixas. Todos os recursos de imagem são declarados na [marcação da faixa](windowsribbon-schema.md) de lista ou consultados de um aplicativo host da faixa de Ribbon.

Para o Windows 8 e posterior, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network Graphics) com transparência.

Para o Windows 7 e versões anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado no Windows.

> [!Note]  
> Um erro de compilação pode ocorrer se um formato de imagem sem suporte for fornecido para a estrutura.

 

## <a name="image-sizes"></a>Tamanhos de imagem

Para fornecer maior flexibilidade para layouts de controle da faixa de opção ao redimensionar uma janela de aplicativo, a estrutura da faixa de faixas aceita e renderiza imagens em um dos dois tamanhos: grande ou pequena.

As imagens a seguir ilustram um aplicativo de faixa de opções que dá suporte a vários tamanhos de faixa de opção por meio de layouts de controle flexíveis e a substituição de imagens grandes com imagens pequenas, quando disponíveis.

A captura de tela a seguir mostra a faixa de opções com imagens grandes para os controles de zoom.

![captura de tela mostrando uma faixa de faixas que usa imagens grandes para os controles de zoom.](images/overviews/imageresources-largeimage.png)

A captura de tela a seguir mostra a mesma faixa de opções redimensionada com imagens pequenas para os controles de zoom

![captura de tela mostrando uma faixa de faixas que usa imagens pequenas para os controles de zoom.](images/overviews/imageresources-smallimage.png)

A captura de tela a seguir mostra a faixa de opções no estado oculto. A faixa de opção fica oculta quando todos os layouts de controle potenciais foram esgotados e a faixa de faixas não pode ser renderizada com um espaço de trabalho de aplicativo utilizável.

![captura de tela mostrando uma faixa de faixas recolhida.](images/overviews/imageresources-noimage.png)

Para qualquer imagem, o tamanho exato do pixel depende da resolução de vídeo ou pontos por polegada (DPI) do monitor que está sendo usado. Às 96 dpi, as imagens grandes são de 32 a 16 pixels de tamanho e as imagens pequenas têm um tamanho de 16x16 pixels. Os tamanhos de imagem aumentam de maneira linear em relação ao DPI, conforme ilustrado na tabela a seguir.



| EXIBI     | Imagem pequena  | Imagem grande  |
|---------|--------------|--------------|
| 96 dpi  | 16x16 pixels | 32x32 pixels |
| 120 dpi | 20x20 pixels | 40x40 pixels |
| 144 dpi | 24x24 pixels | 48x48 pixels |
| 192 DPI | 32x32 pixels | 64 x 64 pixels |



 

A estrutura da faixa de faixas dimensiona os recursos de imagem conforme necessário. No entanto, como o redimensionamento pode gerar artefatos indesejáveis e degradação de imagem, é altamente recomendável que o aplicativo forneça um pequeno conjunto de recursos de imagem que abrangem várias configurações de DPI usadas com frequência. Se uma correspondência exata não for encontrada, a imagem mais próxima será dimensionada ou reduzida verticalmente.

Para facilitar isso, os recursos de imagem podem ser declarados na marcação da faixa de faixas usando um conjunto de elementos [**Image**](windowsribbon-element-image.md) para cada elemento [**Command**](windowsribbon-element-command.md) . Em tempo de execução, a estrutura seleciona a imagem a ser exibida com base no atributo *MinDPI* de cada elemento **Image** .

> [!IMPORTANT]
>
> Quando uma coleção de recursos de imagem que são projetados para dar suporte a configurações de dpi de tela específicas é fornecida à estrutura da faixa de opções por meio de um conjunto de elementos [**Image**](windowsribbon-element-image.md) , a estrutura usa a **imagem** com um valor de atributo *MinDPI* que corresponde à configuração de dpi de tela atual.
>
> Se nenhum elemento [**Image**](windowsribbon-element-image.md) for declarado com um valor *MinDPI* que corresponda à configuração de dpi de tela atual, a estrutura selecionará a **imagem** que tem o valor de *MinDPI* mais próximo menor que a configuração de dpi de tela atual e dimensionará o recurso de imagem para cima. Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi de tela atual, a estrutura escolherá o valor de *MinDPI* mais próximo maior que a configuração de dpi de tela atual e dimensionará o recurso de imagem para baixo.

 

O exemplo a seguir ilustra como declarar um conjunto de imagens para acomodar vários tamanhos de faixa de opções e configurações do sistema.


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



Se as imagens declaradas na marcação forem invalidadas em tempo de execução por qualquer motivo, o aplicativo host será consultado em busca de novas imagens. Quando essas imagens são geradas e carregadas programaticamente, o aplicativo deve tentar retornar imagens que são dimensionadas de acordo com os tamanhos de ícone do sistema padrão determinados pela [ \_ métrica do sistema SM CXICON](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).

> [!Note]  
> Imagens grandes têm um tamanho de SM \_ CXICON por SM \_ CXICON e imagens pequenas têm um tamanho de SM \_ CXICON/2 por SM \_ CXICON/2.

 

## <a name="color-depth-transparency-and-contrast"></a>Intensidade de cor, transparência e contraste

Espera-se que as imagens regulares estejam no formato de pixel ARGB de 32 bits por pixel (BPP) e dimensionadas para o tamanho do ícone do sistema padrão. Esse formato dá suporte à transparência e à suavização (usando 8 bits por canal).

> [!WARNING]
> Muitas ferramentas de edição de imagens não preservam o canal alfa de 8 bits de ordem mais alta ao carregar ou salvar imagens de 32 BPP.

 

Para que uma imagem seja exibida corretamente no modo de alto contraste, ela deve estar em um formato de pixel em palete 4 BPP. Quando a imagem é renderizada, a estrutura da faixa de faixas remapeia cores específicas com base no contexto de alto contraste da imagem.

A tabela a seguir lista o comportamento de renderização de cores de alto contraste da estrutura.



Cor do pixel

Valor RGB

Comportamento

Plano de fundo branco

Plano de fundo escuro

MAGENTA

800080

Transparente

Transparente

Afasta

000000

WINDOWTEXT de cor \_

Branco

Branco

FFFFFF

janela de cores \_

Afasta

CINZA-ESCURO

808080

3DSHADOW de cor \_

3DSHADOW de cor \_

TONALIDADE

C0C0C0

3DFACE de cor \_

3DFACE de cor \_

CINZA-CLARO

DFDFDF

3DLIGHT de cor \_

3DLIGHT de cor \_

AZUL-ESCURO

000080

N/D

Branco



 

Para obter mais informações sobre os formatos de imagem com suporte na estrutura da faixa de opções, consulte o seguinte:

-   [Estrutura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) -descreve o formato de pixel ARGB de 32 bpp.
-   [Função CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) – descreve como criar uma imagem de formato de pixel ARGB de 32 bpp.
-   [Função LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) – descreve como carregar uma imagem de formato de pixel ARGB de 32 bpp.

## <a name="accessibility"></a>Acessibilidade

Depender de recursos de imagem para fornecer informações, transmitir funcionalidade de controle e expor o estado do aplicativo, aumenta a necessidade de requisitos de acessibilidade durante o design e o desenvolvimento de aplicativos.

Para suporte de alto contraste básico, a faixa de faixas permite que um conjunto separado de arquivos de imagem seja exibido quando um tema de alto contraste está ativo. Essas imagens podem ser 32 BPP ou 4 BPP, com cores mapeadas para uma paleta especial em que as cores escuras e claras são invertidas dependendo das cores de primeiro e segundo plano do tema de alto contraste ativo.

O exemplo a seguir demonstra como os recursos de imagem de alto contraste são declarados na marcação da faixa de opções:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[\_SmallImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[\_LargeImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[\_SmallHighContrastImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[\_LargeHighContrastImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 