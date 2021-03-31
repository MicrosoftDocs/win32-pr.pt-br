---
description: Define os vários tipos de formatos de superfície.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664025"
---
# <a name="d3dformat"></a>D3DFORMAT

Define os vários tipos de formatos de superfície.

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a>Comentários

Há vários tipos de formatos:

-   [Formatos de BackBuffer ou de exibição](#backbuffer-or-display-formats)
-   [Formatos de buffer](#buffer-formats)
-   [Formatos de textura compactados DXTn](#dxtn-compressed-texture-formats)
-   [Formatos de ponto flutuante](#floating-point-formats)
-   [Formatos FOURCC](#fourcc-formats)
-   [Formatos IEEE](#ieee-formats)
-   [Formatos mistos](#mixed-formats)
-   [Formatos assinados](#signed-formats)
-   [Formatos não assinados](#unsigned-formats)
-   [Outras](#other)

Todos os formatos são listados da esquerda para a direita, o bit mais significativo para um bit menos significativo. Por exemplo, **D3DFORMAT \_ ARGB** é ordenada do canal de bits mais significativo a (alfa), para o canal de bits B menos significativo (azul). Ao percorrer os dados da superfície, os dados são armazenados na memória do bit menos significativo para o bit mais significativo, o que significa que a ordem do canal na memória é de um bit menos significativo (azul) para o bit mais significativo (alfa).

O valor padrão para formatos que contêm canais indefinidos (G16R16, A8 e assim por diante) é 1. A única exceção é o formato A8, que é inicializado como 000 para os três canais de cor.

A ordem dos bits é do byte mais significativo primeiro, portanto D3DFMT \_ A8L8 indica que o byte alto desse formato de 2 bytes é Alfa. **D3DFMT \_ D16** indica um valor inteiro de 16 bits e uma superfície de bloqueáveis de aplicativo.

Formatos de pixel foram escolhidos para habilitar a expressão de formatos de extensão definidos pelo fornecedor de hardware, bem como para incluir o método FOURCC bem estabelecido. O conjunto de formatos compreendido pelo tempo de execução do Direct3D é definido por D3DFORMAT.

Observe que os formatos são fornecidos por fornecedores de hardware independentes (IHVs) e muitos códigos FOURCC não estão listados. Os formatos nessa enumeração são exclusivos, pois são aprovados pelo tempo de execução, o que significa que o rasterizador de referência funcionará em todos esses tipos. Os formatos fornecidos por IHV serão compatíveis com os IHVs individuais em uma base de cartão a cartão.

### <a name="backbuffer-or-display-formats"></a>Formatos de BackBuffer ou de exibição

Esses formatos são os únicos formatos válidos para um buffer de fundo ou uma exibição.



| Formatar      | Buffer de fundo | Monitor                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (somente no modo de tela inteira) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Formatos de buffer

Os buffers de profundidade, estêncil, vértice e índice têm formatos exclusivos.



| Sinalizadores de buffer               | Valor | Formatar                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ bloqueáveis**  | 70    | profundidade de bit z-buffer de 16 bits.                                                                                                                    |
| **D3DFMT \_ D32**            | 71    | 32 bits z-profundidade de bit do buffer.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | profundidade de bit z-buffer de 16 bits, em que 15 bits são reservados para o canal de profundidade e 1 bit é reservado para o canal de estêncil.                     |
| **D3DFMT \_ D24S8**          | 75    | 32 bits z-profundidade de bit do buffer usando 24 bits para o canal de profundidade e 8 bits para o canal do estêncil.                                             |
| **D3DFMT \_ D24X8**          | 77    | 32 bits z-profundidade de bit do buffer usando 24 bits para o canal de profundidade.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | 32 bits z-profundidade de bit do buffer usando 24 bits para o canal de profundidade e 4 bits para o canal do estêncil.                                             |
| **D3DFMT \_ D32F \_ bloqueáveis** | 82    | Um formato bloqueáveis em que o valor de profundidade é representado como um número de ponto flutuante padrão IEEE.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Um formato não bloqueáveis que contém 24 bits de profundidade (em um formato de ponto flutuante de 24 bits-20e4) e 8 bits de estêncil.                        |
| **D3DFMT \_ D32 \_ bloqueáveis**  | 84    | Um buffer de profundidade de bloqueáveis de 32 bits. **Diferenças entre o Direct3D 9 e o Direct3d 9EX:** Esse sinalizador está disponível somente no Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ bloqueáveis**   | 85    | Um buffer de estêncil de 8 bits bloqueáveis. **Diferenças entre o Direct3D 9 e o Direct3d 9EX:** Esse sinalizador está disponível somente no Direct3D 9Ex.<br/> |
| **D3DFMT \_ D16**            | 80    | profundidade de bit z-buffer de 16 bits.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Descreve uma superfície de buffer de vértice.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | profundidade de bit de buffer de índice de 16 bits.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | profundidade de bit de buffer de índice de 32 bits.                                                                                                                |



 

Todos os formatos de estêncil de profundidade, exceto D3DFMT \_ D16 \_ bloqueáveis, não indicam nenhuma ordenação de bits específica por pixel, e o driver tem permissão para consumir mais do que o número indicado do canal de bits por profundidade (mas não do canal de estêncil).

### <a name="dxtn-compressed-texture-formats"></a>Formatos de textura compactados DXTn

Esses sinalizadores são usados para texturas compactadas:



| Sinalizadores de textura compactados do DXTn | Valor                          | Formatar                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC (' D', ' X ', ' T', ' 1 ') | Formato de textura de compactação DXT1 |
| **D3DFMT \_ DXT2**              | MAKEFOURCC (' D', ' X ', ' T', ' 2 ') | Formato de textura de compactação DXT2 |
| **D3DFMT \_ DXT3**              | MAKEFOURCC (' D', ' X ', ' T', ' 3 ') | Formato de textura de compactação DXT3 |
| **D3DFMT \_ DXT4**              | MAKEFOURCC (' D', ' X ', ' T', ' 4 ') | Formato de textura de compactação DXT4 |
| **D3DFMT \_ DXT5**              | MAKEFOURCC (' D', ' X ', ' T', ' 5 ') | Formato de textura de compactação DXT5 |



 

O tempo de execução não permitirá que um aplicativo crie uma superfície usando um formato DXTn, a menos que as dimensões de superfície sejam múltiplos de 4. Isso se aplica a superfícies sem formatação automática, destinos de renderização, texturas 2D, texturas de cubo e texturas de volume.

### <a name="floating-point-formats"></a>Formatos de Floating-Point

Esses sinalizadores são usados para formatos de superfície de ponto flutuante. Esses formatos de 16 bits por canal também são conhecidos como formatos s10e5.



| Sinalizadores de ponto flutuante      | Valor | Formatar                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | formato float de 16 bits usando 16 bits para o canal vermelho.                                   |
| **D3DFMT \_ G16R16F**       | 112   | formato float de 32 bits usando 16 bits para o canal vermelho e 16 bits para o canal verde. |
| **D3DFMT \_ A16B16G16R16F** | 113   | formato float de 64 bits usando 16 bits para cada canal (alfa, azul, verde, vermelho).        |



 

### <a name="fourcc-formats"></a>Formatos FOURCC

Os dados em um formato FOURCC são dados compactados.

### <a name="makefourcc"></a>MAKEFOURCC

Segue uma macro para gerar códigos de quatro caracteres:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Aqui estão os formatos FOURCC definidos:



| Sinalizadores FOURCC              | Valor                          | Formatar                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ Multi2 \_ ARGB8** | MAKEFOURCC (' M', ' E ', ' T', ' 1 ')    | Textura Multielemento (não compactada)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC (' G ', ' R ', ' G ', ' B ') | Um formato RGB empacotado de 16 bits análogo a YUY2 (Y0U0, Y1V0, Y2U2 e assim por diante). Ele requer um par de pixels para representar corretamente o valor de cor. O primeiro pixel do par contém 8 bits de verde (nos 8 bits altos) e 8 bits de vermelho (nos 8 bits baixos). O segundo pixel contém 8 bits de verde (nos 8 bits altos) e 8 bits de azul (nos 8 bits baixos). Juntos, os dois pixels compartilham os componentes vermelho e azul, enquanto cada um tem um componente verde exclusivo (G0R0, G1B0, G2R2 e assim por diante). A amostra de textura não normaliza as cores ao procurar um sombreador de pixel; Eles permanecem no intervalo de 0,0 f a 255.0 f. Isso é verdadeiro para todos os modelos de sombreador de pixel programável. Para o sombreador de pixel de função fixa, o hardware deve normalizar para o intervalo de 0. f para 1. f e, essencialmente, tratá-lo como a textura YUY2. O hardware que expõe esse formato deve ter o membro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) definido como um valor capaz de lidar com esse intervalo. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC (' R ', ' G ', ' B ', ' G ') | Um formato RGB empacotado de 16 bits análogo a UYVY (U0Y0, V0Y1, U2Y2 e assim por diante). Ele requer um par de pixels para representar corretamente o valor de cor. O primeiro pixel do par contém 8 bits de verde (nos 8 bits baixos) e 8 bits de vermelho (nos alta 8 bits). O segundo pixel contém 8 bits de verde (nos 8 bits baixos) e 8 bits de azul (nos alta 8 bits). Juntos, os dois pixels compartilham os componentes vermelho e azul, enquanto cada um tem um componente verde exclusivo (R0G0, B0G1, R2G2 e assim por diante). A amostra de textura não normaliza as cores ao procurar um sombreador de pixel; Eles permanecem no intervalo de 0,0 f a 255.0 f. Isso é verdadeiro para todos os modelos de sombreador de pixel programável. Para o sombreador de pixel de função fixa, o hardware deve normalizar para o intervalo de 0. f para 1. f e, essencialmente, tratá-lo como a textura YUY2. O hardware que expõe esse formato deve ter o membro PixelShader1xMaxValue de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) definido como um valor capaz de lidar com esse intervalo.     |
| **D3DFMT \_ UYVY**          | MAKEFOURCC (' U ', ' Y ', ' V ', ' Y ') | Formato UYVY (conformidade PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC (' Y ', ' U ', ' Y ', ' 2 ') | Formato YUY2 (conformidade PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formatos IEEE

Esses sinalizadores são usados para formatos de superfície de ponto flutuante. Esses formatos de 32 bits por canal também são conhecidos como formatos s23e8.



| Sinalizadores de ponto flutuante      | Valor | Formatar                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | formato float de 32 bits usando 32 bits para o canal vermelho.                                   |
| **D3DFMT \_ G32R32F**       | 115   | formato float de 64 bits usando 32 bits para o canal vermelho e 32 bits para o canal verde. |
| **D3DFMT \_ A32B32G32R32F** | 116   | formato float de 128 bits usando 32 bits para cada canal (alfa, azul, verde, vermelho).       |



 

### <a name="mixed-formats"></a>Formatos mistos

Os dados em formatos mistos podem conter uma combinação de dados não assinados e dados assinados.



| Sinalizadores de formato misto      | Valor | Formatar                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | rebatida de 16 bits-formato de mapa com luminância usando 6 bits para luminância e 5 bits cada para v e você. |
| **D3DFMT \_ X8L8V8U8**    | 62    | rebatida de 32 bits-formato de mapa com luminância usando 8 bits para cada canal.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | rebatida de 32 bits – mapeie o formato usando 2 bits para alfa e 10 bits cada para w, v e você.                |



 

### <a name="signed-formats"></a>Formatos assinados

Os dados em um formato assinado podem ser positivos e negativos. Os formatos assinados usam combinações de (U), (V), (W) e (Q) dados.



| Sinalizadores de formato assinados      | Valor | Formatar                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | rebatida de 16 bits – mapeie formato usando 8 bits cada para você e para os dados de v.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | rebatida de 32 bits-formato de mapa usando 8 bits para cada canal.                                                     |
| **D3DFMT \_ V16U16**       | 64    | rebatida de 32 bits-formato de mapa usando 16 bits para cada canal.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | rebatida de 64 bits-formato de mapa usando 16 bits para cada componente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | formato de compactação normal de 16 bits. A amostra de textura computa o canal C de: C = sqrt (1-U ²-V ²). |



 

### <a name="unsigned-formats"></a>Formatos não assinados

Os dados em um formato não assinado devem ser positivos. Os formatos não assinados usam combinações de (R) Ed, (G) reen, (B) lue, (A) lpha, (L) uminance e (P) Alette Data. Os dados da paleta também são chamados de dados indexados por cor porque os dados são usados para indexar uma paleta de cores.



| Sinalizadores de formato não assinados             | Valor | Formatar                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | formato de pixel RGB de 24 bits com 8 bits por canal.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | formato de pixel ARGB de 32 bits com Alfa, usando 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | formato de pixel RGB de 32 bits, em que 8 bits são reservados para cada cor.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | formato de pixel RGB de 16 bits com 5 bits para vermelho, 6 bits para verde e 5 bits para azul.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | formato de pixel de 16 bits, em que os 5 bits são reservados para cada cor.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | formato de pixel de 16 bits, em que 5 bits são reservados para cada cor e 1 bit é reservado para alfa.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | formato de pixel ARGB de 16 bits com 4 bits para cada canal.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | formato de textura RGB de 8 bits usando 3 bits para vermelho, 3 bits para verde e 2 bits para azul.                                                                                     |
| **D3DFMT \_ a8**                    | 28    | somente alfa de 8 bits.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | formato de textura ARGB de 16 bits usando 8 bits para alfa, 3 bits cada para vermelho e verde e 2 bits para azul.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | formato de pixel RGB de 16 bits usando 4 bits para cada cor.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | formato de pixel de 32 bits usando 10 bits para cada cor e 2 bits para alfa.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | formato de pixel ARGB de 32 bits com Alfa, usando 8 bits por canal.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | formato de pixel RGB de 32 bits, em que 8 bits são reservados para cada cor.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | formato de pixel de 32 bits usando 16 bits cada para verde e vermelho.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | formato de pixel de 32 bits usando 10 bits cada para vermelho, verde e azul e 2 bits para alfa.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | formato de pixel de 64 bits usando 16 bits para cada componente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | cor de 8 bits indexada com 8 bits de alfa.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | cor de 8 bits indexada.                                                                                                                                                      |
| **\_L8 D3DFMT**                    | 50    | apenas luminância de 8 bits.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | apenas luminância de 16 bits.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 bits usando 8 bits cada para alfa e luminância.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8 bits usando 4 bits cada para alfa e luminância.                                                                                                                          |
| **D3DFMT \_ a1**                    | 118   | monocromático de 1 bit. **Diferenças entre o Direct3D 9 e o Direct3d 9EX:** Esse sinalizador está disponível somente no Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_ Bias** | 119   | 2,8-ponto fixo com tendência. **Diferenças entre o Direct3D 9 e o Direct3d 9EX:** Esse sinalizador está disponível somente no Direct3D 9Ex.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Formato binário que indica que os dados não têm nenhum tipo inerente. **Diferenças entre o Direct3D 9 e o Direct3d 9EX:** Esse sinalizador está disponível somente no Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Outro

Esse sinalizador é usado para formatos indefinidos.



| Outros sinalizadores         | Valor | Formatar                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ desconhecido** | 0     | Formato de superfície desconhecido |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




