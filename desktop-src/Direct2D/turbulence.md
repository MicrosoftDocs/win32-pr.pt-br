---
title: Efeito de turbulência
description: Use o efeito turbulência para gerar um bitmap com base na função de ruído Perl.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- efeito de turbulência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f2aa58be48c759956fe3522812d7ad6c3e9989
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468593"
---
# <a name="turbulence-effect"></a>Efeito de turbulência

Use o efeito turbulência para gerar um bitmap com base na função de ruído Perl.

O efeito turbulência não tem nenhuma imagem de entrada.

O CLSID para esse efeito é CLSID \_ D2D1Turbulence.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de ruído](#noise-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![captura de tela de exemplo de efeito mostrando a saída do efeito turbulência.](images/32-turbulence.png)

O efeito turbulência computa a soma de um ou mais octaves da função de ruído do Perlm. O ruído de Perl é uma função pseudo aleatória cujo valor depende da frequência, da posição e do valor de semente. O efeito gera os valores RGBA usando uma dessas equações.

Se você selecionar o modo de ruído de soma de ruído de D2D1 \_ turbulência, \_ \_ \_ o efeito usará essa equação.

![Captura de tela que mostra a função turbulência usada para gerar um bitmap.](images/turbulence-equation1.png)

Se você selecionar o modo de ruído D2D1 \_ turbulência de \_ ruído \_ turbulência, o efeito usará essa equação.

![a função turbulência usada para gerar um bitmap.](images/turbulence-equation2.png)

> [!Note]  
> A `PerlinNoise` função tem um intervalo de \[ -1, 1 \] .

 

Esse efeito gera valores de pixel no alfa precalculado.

## <a name="effect-properties"></a>Propriedades do efeito




| Nome de exibição e enumeração de índice | Descrição | 
|------------------------------------|-------------|
| Deslocamento<br /> D2D1_TURBULENCE_PROP_OFFSET<br /> | As coordenadas em que a saída turbulência é gerada.<br /> O algoritmo usado para gerar o ruído de Perl é dependente da posição, portanto, um deslocamento diferente resulta em uma saída diferente. Essa propriedade não está vinculada e as unidades são especificadas em DIPs <br /><blockquote>[!Note]<br />O deslocamento não tem o mesmo efeito que uma tradução, pois a saída da função de ruído é infinita e a função será encodificada ao lado do bloco.</blockquote><br /> O tipo é D2D1_VECTOR_2F.<br /> O valor padrão é {0,0 f, 0,0 f}.<br /> | 
| Tamanho<br /> D2D1_TURBULENCE_PROP_SIZE<br /> | O tamanho da saída do turbulência.<br /> Essa propriedade não está vinculada e as unidades são especificadas em DIPs <br /><br /> O tipo é D2D1_VECTOR_2F.<br /> O valor padrão é {0,0 f, 0,0 f}.<br /> | 
| BaseFrequency<br /> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br /> | As frequências de base nas direções X e Y. Esta propriedade é um float e deve ser maior que 0. As unidades são especificadas em 1/DIPs. <br /> Um valor de 1 (1/DIPs) para a frequência base resulta no ruído de Perl, concluindo um ciclo inteiro entre dois pixels. A interpolação de atenuação para esses pixels resulta em pixels completamente aleatórios, já que não há nenhuma correlação entre os pixels.<br /> Um valor de 0,1 (1/DIPs) para a frequência base, a função de ruído de Perlm se repete a cada 10 DIPs. Isso resulta em uma correlação entre pixels e o efeito típico de turbulência é visível.<br /> O tipo é D2D1_VECTOR_2F.<br /> O valor padrão é {0,01 f, 0,01 f}.<br /> | 
| NumOctaves<br /> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br /> | O número de octaves para a função de ruído. Esta propriedade é um UINT32 e deve ser maior que 0.<br /> O tipo é UINT32.<br /> O valor padrão é 1.<br /> | 
| Seed<br /> D2D1_TURBULENCE_PROP_SEED<br /> | A semente do gerador de pseudo aleatório. Esta propriedade não está associada.<br /> O tipo é UINT32.<br /> O valor padrão é 0.<br /> | 
| Ruído<br /> D2D1_TURBULENCE_PROP_NOISE<br /> | O modo de ruído turbulência. Essa propriedade pode ser <em>fractal Sum</em> ou <em>turbulência</em>. Indica se um bitmap deve ser gerado com base no ruído de fractal ou na função turbulência. Consulte <a href="#noise-modes">modos de ruído</a> para obter mais informações. <br /> O tipo é D2D1_TURBULENCE_NOISE.<br /> O valor padrão é D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br /> | 
| Costura<br /> D2D1_TURBULENCE_PROP_STITCHABLE<br /> | Ativa ou desativa o grampeamento. A frequência base é ajustada para que o bitmap de saída possa ser grampeado. Isso será útil se você quiser dividir várias cópias da saída do efeito turbulência.<ul><li>True o bitmap de saída pode ser enquadrado (usando o efeito de bloco) sem a aparência de emendas. A frequência base é ajustada para que o bitmap de saída possa ser grampeado.</li><li>False a frequência base não é ajustada, portanto, as fendas podem aparecer entre os blocos se o bitmap for enlado.</li></ul><br /> O tipo é BOOL.<br /> O valor padrão é FALSE.<br /> | 




 

## <a name="noise-modes"></a>Modos de ruído



| Enumeração                           | Descrição                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| \_Soma de \_ fractal de ruído d2d1 turbulência \_ \_ | Computa uma soma do octaves, deslocando o intervalo de saída de \[ -1, 1 \] , para \[ 0, 1 \] . |
| D2D1 \_ turbulência \_ Noise \_ turbulência   | Computa uma soma do valor absoluto de cada Octave.                                  |



 

> [!Note]  
> Nenhum modo contém um fixe explícito dos valores de saída.

 

## <a name="output-bitmap"></a>Bitmap de saída

Esse efeito gera um bitmap de tamanho logicamente infinito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

