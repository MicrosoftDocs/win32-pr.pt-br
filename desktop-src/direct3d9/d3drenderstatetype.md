---
description: Estados de renderização definem estados de configuração para todos os tipos de processamento de vértice e pixel.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeração D3DRENDERSTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343061"
---
# <a name="d3drenderstatetype-enumeration"></a>Enumeração D3DRENDERSTATETYPE

Estados de renderização definem estados de configuração para todos os tipos de processamento de vértice e pixel. Alguns estados de renderização configuram o processamento de vértice e outros configuram o processamento de pixel (consulte Estados de [renderização (Direct3D 9)](render-states.md)). Os estados de renderização podem ser salvos e restaurados usando stateblocks (consulte Estado de salvar e restaurar blocos de estado [(Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

Estado de buffer de profundidade como um membro do tipo enumerado [**D3DZBUFFERTYPE.**](./d3dzbuffertype.md) De definir esse estado como D3DZB TRUE para habilitar o \_ buffer z, D3DZB USEW para habilitar \_ w-buffering ou D3DZB FALSE para desabilitar o buffer de \_ profundidade.

O valor padrão para esse estado de renderização será D3DZB TRUE se um estêncil de profundidade tiver sido criado junto com a cadeia de permuta definindo o membro \_ EnableAutoDepthStencil da estrutura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) como **TRUE** e D3DZB FALSE caso \_ contrário.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

Um ou mais membros do [**tipo enumerado D3DFILLMODE.**](./d3dfillmode.md) O valor padrão é D3DFILL \_ SOLID.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Um ou mais membros do tipo [**enumerado D3DSHADEMODE.**](./d3dshademode.md) O valor padrão é D3DSHADE \_ GOURAUD.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**TRUE** para habilitar o aplicativo a gravar no buffer de profundidade. O valor padrão é **TRUE.** Esse membro permite que um aplicativo impeça que o sistema atualiza o buffer de profundidade com novos valores de profundidade. Se **for false**, as comparações de profundidade ainda serão feitas de acordo com o estado de renderização D3DRS \_ ZFUNC, supondo que o buffer de profundidade esteja ocorrendo, mas os valores de profundidade não são gravados no buffer.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**True** para habilitar testes alfa por pixel. Se o teste passar, o pixel será processado pelo buffer de quadros. Caso contrário, todo o processamento do buffer de quadros será ignorado para o pixel.

O teste é feito comparando o valor alfa de entrada com o valor alfa de referência, usando a função de comparação fornecida pelo \_ estado de RENDERIZAÇÃO D3DRS ALPHAFUNC. O valor alfa de referência é determinado pelo valor definido para D3DRS \_ ALPHAREF. Para obter mais informações, consulte [Alpha Test State (Direct3D 9)](alpha-testing-state.md).

O valor padrão desse parâmetro é **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

O valor padrão é **true**, que habilita o desenho do último pixel em uma linha. Para evitar o desenho do último pixel, defina esse valor como **false**. Para obter mais informações, consulte [estrutura de tópicos e estado de preenchimento (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) . O valor padrão é D3DBLEND \_ One.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) . O valor padrão é D3DBLEND \_ zero.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS de \_ seleção**
</dt> <dd>

Especifica como os triângulos voltados para trás são eliminados, se for. Isso pode ser definido como um membro do tipo enumerado [**D3DCULL.**](./d3dcull.md) O valor padrão é D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**
</dt> <dd>

Um membro do tipo [**enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) O valor padrão é D3DCMP \_ LESSEQUAL. Esse membro permite que um aplicativo aceite ou rejeite um pixel, com base em sua distância da câmera.

O valor de profundidade do pixel é comparado com o valor do buffer de profundidade. Se o valor de profundidade do pixel passar na função de comparação, o pixel será gravado.

O valor de profundidade será gravado no buffer de profundidade somente se o estado de renderização for **TRUE.**

Os rasterizadores de software e muitos aceleradores de hardware funcionam mais rapidamente se o teste de profundidade falhar, pois não há necessidade de filtrar e modular a textura se o pixel não for renderizado.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**ALFAREF D3DRS \_**
</dt> <dd>

Valor que especifica um valor alfa de referência em relação aos pixels testados quando o teste alfa está habilitado. Esse é um valor de 8 bits colocado nos 8 bits baixos do valor de estado de renderização DWORD. Os valores podem variar de 0x00000000 a 0x000000FF. O valor padrão é 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**ALFAFUNC D3DRS \_**
</dt> <dd>

Um membro do tipo [**enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) O valor padrão é D3DCMP \_ ALWAYS. Esse membro permite que um aplicativo aceite ou rejeite um pixel, com base em seu valor alfa.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**True** para habilitar o pontilhamento. O valor padrão é **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**True** para habilitar a transparência com combinação alfabética. O valor padrão é **FALSE**.

O tipo de mistura alfa é determinado pelos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLEND e \_ D3DRS DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**
</dt> <dd>

**True** para habilitar a mesclagem de neblina. O valor padrão é **FALSE**. Para obter mais informações sobre como usar a mistura de neblina, consulte [neblina](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**True** para habilitar os realces especulares. O valor padrão é **FALSE**.

Os realces especulares são calculados como se cada vértice no objeto que está sendo aceso estiver na origem do objeto. Isso fornece os resultados esperados, desde que o objeto seja modelado em volta da origem e a distância da luz para o objeto seja relativamente grande. Em outros casos, os resultados são indefinidos.

Quando esse membro é definido como **true**, a cor especular é adicionada à cor base após a textura em cascata, mas antes da mistura alfa.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**
</dt> <dd>

Valor cujo tipo é [**D3DCOLOR**](d3dcolor.md). O valor padrão é 0. Para obter mais informações sobre a cor de neblina, consulte [cor de neblina (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**
</dt> <dd>

A fórmula de neblina a ser usada para sombra de pixel. Defina como um dos membros do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . O valor padrão é D3DFOG \_ None. Para obter mais informações sobre pixel pixel pixel, consulte [Pixel Pixel (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRSSTART \_**
</dt> <dd>

Profundidade na qual os efeitos de pixel ou vértice começam para o modo linear de linear. O valor padrão é 0,0f. A profundidade é especificada no espaço do mundo para o vértice e o espaço do dispositivo \[ 0,0, 1,0 ou espaço mundial para \] pixel pixel. Para pixel pixel pixel, esses valores estão no espaço do dispositivo quando o sistema usa z para cálculos de pontos de cálculo e espaço do mundo quando o sistema está usando o olho relativo ao olho (w-world). Para obter mais informações, [consulte Parâmetros de Base (Direct3D 9)](fog-parameters.md) e [Eye-Relative versus Profundidade baseada em Z.](pixel-fog.md)

Os valores para esse estado de renderização são valores de ponto flutuante. Como [**o método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve lançar uma variável que contenha o valor, conforme mostrado no exemplo de código a seguir.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**\_D3DRSDISTAND**
</dt> <dd>

Profundidade na qual os efeitos de pixel ou vértice terminam para o modo linear de linear. O valor padrão é 1,0f. A profundidade é especificada no espaço do mundo para o vértice e o espaço do dispositivo \[ 0,0, 1,0 ou espaço mundial para \] pixel pixel. Para pixel pixel pixel, esses valores estão no espaço do dispositivo quando o sistema usa z para cálculos de lodo e no espaço do mundo quando o sistema está usando o olho relativo (w-world). Para obter mais informações, [consulte Parâmetros de Base (Direct3D 9)](fog-parameters.md) e [Eye-Relative versus Profundidade baseada em Z.](pixel-fog.md)

Os valores para esse estado de renderização são valores de ponto flutuante. Como [**o método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve lançar uma variável que contenha o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**DENSIDADE DE \_ D3DRS**
</dt> <dd>

Densidade de roda para pixel ou vértice usada nos modos de união exponencial (D3DFOG \_ EXP e D3DFOG \_ EXP2). Os valores de densidade válidos variam de 0,0 a 1,0. O valor padrão é 1.0. Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).

Os valores para esse estado de renderização são valores de ponto flutuante. Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**True** para habilitar a neblina de vértice com base em intervalos. O valor padrão é **false**; nesse caso, o sistema usa a neblina baseada em profundidade. Na neblina baseada em intervalo, a distância de um objeto do visualizador é usada para computar efeitos de neblina, não a profundidade do objeto (ou seja, a coordenada z) na cena. Na neblina baseada em intervalo, todos os métodos de neblina funcionam normalmente, exceto pelo fato de que eles usam o intervalo em vez de profundidade nos cálculos.

Range é o fator correto a ser usado para cálculos de neblina, mas a profundidade geralmente é usada, pois o intervalo é demorado para computar e a profundidade geralmente já está disponível. O uso de profundidade para calcular a neblina tem o efeito indesejável de que a fogginess dos objetos periféricos muda à medida que os olhos do visualizador – nesse caso, a profundidade muda e o intervalo permanece constante.

Como nenhum hardware dá suporte atualmente a neblina com base em intervalos por pixel, a correção de intervalo é oferecida apenas para a neblina de vértice.

Para obter mais informações, consulte [Vertex neblina (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**True** para habilitar a estêncil, ou **false** para desabilitar o estêncil. O valor padrão é **FALSE**. Para obter mais informações, consulte as [técnicas de buffer de estêncil (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

Operação de estêncil a ser executada se o teste de estêncil falhar. Os valores são do tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . O valor padrão é D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Operação de estêncil a ser realizada se o teste de estêncil for aprovado e o teste de profundidade (z-test) falhar. Os valores são do [**tipo enumerado D3DSTENCI DIGIT.**](./d3dstencilop.md) O valor padrão é D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Operação de estêncil a ser realizada se os testes de estêncil e profundidade (z) passarem. Os valores são do [**tipo enumerado D3DSTENCI DIGIT.**](./d3dstencilop.md) O valor padrão é D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Função de comparação para o teste de estêncil. Os valores são do [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) O valor padrão é D3DCMP \_ ALWAYS.

A função de comparação é usada para comparar o valor de referência com uma entrada de buffer de estêncil. Essa comparação se aplica somente aos bits no valor de referência e na entrada de buffer de estêncil que são definidos na máscara de estêncil (definida pelo estado de \_ renderização D3DRS STENCILMASK). Se **TRUE**, o teste de estêncil será aprovado.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Um valor de referência int para o teste de estêncil. O valor padrão é 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Máscara aplicada ao valor de referência e a cada entrada de buffer de estêncil para determinar os bits significativos para o teste de estêncil. A máscara padrão é 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

Máscara de gravação aplicada a valores gravados no buffer do estêncil. A máscara padrão é 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

A cor usada para mesclagem de várias texturas com o argumento de mistura de textura D3DTA \_ TFACTOR ou a \_ operação de mesclagem de textura D3DTOP BLENDFACTORALPHA. O valor associado é uma variável [**D3DCOLOR**](d3dcolor.md) . O valor padrão é opaco branco (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Comportamento de disposição de textura para vários conjuntos de coordenadas de textura. Os valores válidos para esse estado de renderização podem ser qualquer combinação de D3DWRAPCOORD \_ 0 (ou D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (ou D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (ou D3DWRAP \_ W) e D3DWRAPCOORD \_ 3 flags. Isso faz com que o sistema Empacote a direção da primeira, segunda, terceira e quarta dimensões, às vezes chamadas de direções s, t, r e q, para uma determinada textura. O valor padrão para esse estado de renderização é 0 (encapsulamento desabilitado em todas as direções).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**RECORTE D3DRS \_**
</dt> <dd>

**TRUE** para habilitar o recorte primitivo pelo Direct3D ou **FALSE** para desabilitá-lo. O valor padrão é **TRUE.**

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**ILUMINAÇÃO D3DRS \_**
</dt> <dd>

**TRUE** para habilitar a iluminação Direct3D ou **FALSE** para desabilitá-la. O valor padrão é **TRUE.** Somente os vértices que incluem um vértice normal estão corretamente acesos; Vértices que não contêm um normal empregam um produto de ponto de 0 em todos os cálculos de iluminação.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**AMBIENTE D3DRS \_**
</dt> <dd>

Cor da luz do ambiente. Esse valor é do tipo [**D3DCOLOR.**](d3dcolor.md) O valor padrão é 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_D3DRSVERTEXMODE**
</dt> <dd>

Fórmula de leite a ser usada para o vértice. Definido como um membro do tipo enumerado [**D3DFOGMODE.**](./d3dfogmode.md) O valor padrão é D3DFOG \_ NONE.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**True** para habilitar a cor por vértice ou **false** para desabilitá-la. O valor padrão é **true**. Habilitar a cor por vértice permite que o sistema inclua a cor definida para vértices individuais em seus cálculos de iluminação.

Para obter mais informações, consulte os seguintes Estados de renderização:

-   D3DRS \_ DiffuseMaterialSource
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**True** para habilitar os destaques de especular relativos à câmera ou **false** para usar os destaques ortogonal de especulação. O valor padrão é **true**. Os aplicativos que usam projeção ortogonal devem especificar **false**.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**True** para habilitar a normalização automática dos Normals de vértice ou **false** para desabilitá-lo. O valor padrão é **FALSE**. Habilitar esse recurso faz com que o sistema Normalize os Normals dos vértices depois de transformá-los no espaço da câmera, o que pode ser demorado computacionalmente.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DiffuseMaterialSource**
</dt> <dd>

Fonte de cores difusa para cálculos de iluminação. Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . O valor padrão é D3DMCS \_ COLOR1. O valor para esse estado de renderização será usado somente se o \_ estado de RENDERIZAÇÃO D3DRS COLORVERTEX for definido como **true**.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Fonte de cores especular para cálculos de iluminação. Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) O valor padrão é D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Fonte de cor do ambiente para cálculos de iluminação. Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) O valor padrão é D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Fonte de cores emissiva para cálculos de iluminação. Os valores válidos são membros do tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) O valor padrão é D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**VÉRTICE D3DRS \_**
</dt> <dd>

Número de matrizes a ser usado para executar a mesclagem de geometria, se for o caso. Os valores válidos são membros do tipo enumerado [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) O valor padrão é D3DVBF \_ DISABLE.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

Habilita ou desabilita planos de recorte definidos pelo usuário. Os valores válidos são qualquer DWORD no qual o status de cada bit (definido ou não definido) alterna o estado de ativação de um plano de recorte definido pelo usuário correspondente. O bit menos significativo (bit 0) controla o primeiro plano de recorte no índice 0 e os bits subsequentes controlam a ativação de planos de recorte em índices mais altos. Se um bit for definido, o sistema aplicará o plano de recorte apropriado durante a renderização da cena. O valor padrão é 0.

As macros [**D3DCLIPPLANEn**](d3dclipplanen.md) são definidas para fornecer uma maneira conveniente de habilitar os planos de recorte.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**Pontos de D3DRS \_**
</dt> <dd>

Um valor float que especifica o tamanho a ser usado para computação de tamanho de ponto nos casos em que o tamanho do ponto não é especificado para cada vértice. Esse valor não é usado quando o vértice contém o tamanho do ponto. Esse valor estará em unidades de espaço na tela se D3DRS \_ POINTSCALEENABLE for **false**; caso contrário, esse valor estará em unidades de espaço de mundo. O valor padrão é o valor que um driver retorna. Se um driver retornar 0 ou 1, o valor padrão será 64, o que permite emulação de tamanho de ponto de software. Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pontos \_ mínimos**
</dt> <dd>

Um valor float que especifica o tamanho mínimo de primitivos de ponto. Os primitivos de ponto são clamped a esse tamanho durante a renderização. Definir isso com valores menores que 1,0 resulta em pontos que se esgotam quando o ponto não cobre um centro de pixels e a suavização está desabilitada ou sendo processada com intensidade reduzida quando a suavização está habilitada. O valor padrão é 1,0 f. O intervalo para esse valor é maior ou igual a 0,0 f. Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**
</dt> <dd>

valor bool. Quando **true**, as coordenadas de textura dos primitivos de ponto são definidas para que as texturas completas sejam mapeadas em cada ponto. Quando **for falso**, as coordenadas de textura de vértice serão usadas para todo o ponto. O valor padrão é **FALSE**. Você pode obter pontos de pixel único no estilo DirectX 7 definindo D3DRS \_ POINTSCALEENABLE como **FALSE** e D3DRS POINTSIZE como 1.0, que são os valores \_ padrão.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

valor bool que controla a computação de tamanho para primitivos de ponto. Quando **TRUE**, o tamanho do ponto é interpretado como um valor de espaço da câmera e é dimensionado pela função de distância e pelo frustum para exibir o dimensionamento do eixo y doport para calcular o tamanho final do ponto de espaço na tela. Quando **FALSE**, o tamanho do ponto é interpretado como espaço na tela e usado diretamente. O valor padrão é **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto. Ativo somente quando D3DRS \_ POINTSCALEENABLE for **TRUE.** O valor padrão é 1,0f. O intervalo para esse valor é maior ou igual a 0,0f. Como [**o método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve lançar uma variável que contenha o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto. Ativo somente quando D3DRS \_ POINTSCALEENABLE for **TRUE.** O valor padrão é 0,0f. O intervalo para esse valor é maior ou igual a 0,0f. Como [**o método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve lançar uma variável que contenha o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Um valor float que controla a atenuação de tamanho baseado em distância para primitivos de ponto. Ativo somente quando D3DRS \_ POINTSCALEENABLE for **TRUE.** O valor padrão é 0,0 f. O intervalo para esse valor é maior ou igual a 0,0 f. Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

valor bool que determina como as amostras individuais são computadas ao usar um buffer de destino de renderização de multiamostra. Quando definido como **true**, os vários exemplos são computados para que a suavização da cena completa seja executada por amostragem em diferentes posições de exemplo para cada amostra múltipla. Quando definido como **false**, os vários exemplos são todos gravados com o mesmo valor de exemplo, amostrados no pixel Center, que permite a renderização sem alias em um buffer de várias amostras. Esse estado de renderização não tem nenhum efeito ao renderizar para um buffer de exemplo único. O valor padrão é **true**.

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Cada bit nessa máscara, começando pelo bit menos significativo (LSB), controla a modificação de um dos exemplos em um destino de renderização de multiamostrar. Portanto, para um destino de renderização de 8 amostras, o byte baixo contém as oito habilitações de gravação para cada um dos oito exemplos. Esse estado de renderização não tem nenhum efeito ao renderizar para um buffer de exemplo único. O valor padrão é 0xFFFFFFFF.

Esse estado de renderização habilita o uso de um buffer de várias amostras como um buffer de acumulação, fazendo a renderização multipassada de Geometry, em que cada passagem atualiza um subconjunto de amostras.

Se houver n amostras habilitadas com várias amostras e k, a intensidade resultante da imagem renderizada deverá ser k/n. Cada componente RGB de cada pixel é fatorado por k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Define se as bordas do patch usarão o mosaico do estilo flutuante. Os valores possíveis são definidos pelo tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) . O valor padrão é D3DPATCHEDGE \_ DISCRETE.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Depure somente para depurar o monitor. Os valores possíveis são definidos pelo tipo enumerado [**D3DDEBUGMONITORTOKENS.**](./d3ddebugmonitortokens.md) Observe que, se D3DRS DEBUGMONITORTOKEN estiver definido, a chamada será tratada como passando um token para o \_ monitor de depuração. Por exemplo, se - depois de passar D3DDMT ENABLE ou \_ D3DDMT DISABLE para \_ D3DRS DEBUGMONITORTOKEN - outros valores de token são passados, o estado (habilitado ou desabilitado) do monitor de depuração ainda \_ persistirá.

Esse estado só é útil para builds de depuração. O monitor de depuração assume como padrão D3DDMT \_ ENABLE.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**
</dt> <dd>

Um valor float que especifica o tamanho máximo para o qual os sprites de ponto serão fixados. O valor deve ser menor ou igual ao membro MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) e maior ou igual a D3DRS \_ POINTSIZE \_ MIN. O valor padrão é 64,0. Como [**o método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve lançar uma variável que contenha o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

valor bool que habilita ou desabilita a combinação de vértices indexados. O valor padrão é **FALSE**. Quando definido como **TRUE,** a mesclagem de vértice indexada é habilitada. Quando definido como **FALSE,** a mesclagem de vértice indexada é desabilitada. Se esse estado de renderização estiver habilitado, o usuário deverá passar índices de matriz como um DWORD empacotado com cada vértice. Quando o estado de renderização é desabilitado e a combinação de vértices é habilitada por meio do estado VERTEXBLEND D3DRS, é equivalente a ter índices de matriz \_ 0, 1, 2, 3 em cada vértice.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

Valor UINT que habilita uma gravação por canal para o buffer de cores de destino de renderização. Um bit definido resulta no canal de cores que está sendo atualizado durante a renderização 3D. Um bit claro faz com que o canal de cor não seja afetado. Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS COLORWRITEENABLE Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo. Esse estado de renderização não afeta a operação de limpeza. O valor padrão é 0x0000000F.

Os valores válidos para esse estado de renderização podem ser qualquer combinação dos \_ sinalizadores D3DCOLORWRITEENABLE alfa, D3DCOLORWRITEENABLE \_ azul, D3DCOLORWRITEENABLE \_ verde ou D3DCOLORWRITEENABLE \_ vermelho.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Um valor float que controla o fator de interpolação. O valor padrão é 0,0 f. Como o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceita valores DWORD, seu aplicativo deve converter uma variável que contém o valor, conforme mostrado no exemplo de código a seguir.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

O valor usado para selecionar a operação aritmética aplicada quando o estado de renderização de mistura alfa, D3DRS \_ ALPHABLENDENABLE, é definido como **true**. Os valores válidos são definidos pelo tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) . O valor padrão é D3DBLENDOP \_ Add.

Se o \_ recurso de dispositivo D3DPMISCCAPS BLENDOP não tiver suporte, D3DBLENDOP \_ Adicionar será executado.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

N-grau de interpolação da posição do patch. Os valores podem ser D3DDEGREE \_ cúbico (padrão) ou D3DDEGREE \_ linear. Para obter mais informações, consulte [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

Grau de interpolação normal de patch N. Os valores podem ser LINEAR D3DDEGREE \_ (padrão) ou D3DDEGREE \_ QUADTIC. Para obter mais informações, [**consulte D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**TRUE** para habilitar o teste de tesoura **e FALSE** para desabilitá-lo. O valor padrão é **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**
</dt> <dd>

Usado para determinar quanto desvio pode ser aplicado a primitivos co-planares para reduzir o z-fighting. O valor padrão é 0.

bias = (max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

em que max é a inclinação de profundidade máxima do triângulo que está sendo renderizado.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**TRUE** para habilitar a antialiação de linha, **FALSE** para desabilitar a antialiação de linha. O valor padrão é **FALSE**.

Ao renderizar para um destino de renderização multisample, D3DRS ANTIALIASEDLINEENABLE é ignorado e todas as linhas \_ são renderizadas com alias. Use [**ID3DXLine para**](id3dxline.md) renderização de linha antialiasada em um destino de renderização multisample.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Nível mínimo de mosaico. O valor padrão é 1,0f. Consulte [Mosaico (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Nível máximo de mosaico. O valor padrão é 1,0 f. Consulte [mosaico (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Valor para incluí de forma adaptativa, na direção x. O valor padrão é 0,0 f. Consulte [mosaico adaptável](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Valor para incluí de forma adaptativa, na direção y. O valor padrão é 0,0 f. Consulte [ \_ mosaico adaptável](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Valor para incluí de forma adaptativa, na direção z. O valor padrão é 1,0 f. Consulte [ \_ mosaico adaptável](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Valor para incluí de forma adaptativa, na direção w. O valor padrão é 0,0 f. Consulte [ \_ mosaico adaptável](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**True** para habilitar o mosaico adaptável, **false** para desabilitá-lo. O valor padrão é **FALSE**. Consulte [Mosaico \_ adaptável.](tessellation.md)

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**TRUE** habilita a latência de dois lados; **FALSE** a desabilita. O valor padrão é **FALSE**. O aplicativo deve definir D3DRS \_ CULLMODE como D3DCULL NONE para habilitar o modo de \_ estêncil de dois lados. Se a ordem de vento do triângulo for no sentido horário, as operações \_ de STENCIL D3DRS \* serão usadas. Se a ordem de esmaeamento for no sentido anti-horário, as operações \_ de STENCIL do CCW D3DRS \_ serão \* usadas.

Para ver se há suporte para esêncil de dois lados, verifique o membro StencilCaps [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED. Consulte também [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

Operação de estêncil a ser realizada se o teste de estêncil do CCW falhar. Os valores são do [**tipo enumerado D3DSTENCI DIGIT.**](./d3dstencilop.md) O valor padrão é D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Operação de estêncil a ser realizada se o teste de estêncil do CCW for aprovado e o z-test falhar. Os valores são do [**tipo enumerado D3DSTENCI DIGIT.**](./d3dstencilop.md) O valor padrão é D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Operação de estêncil a ser realizada se o esêncil do CCW e os testes z são aprovados. Os valores são do [**tipo enumerado D3DSTENCI DIGIT.**](./d3dstencilop.md) O valor padrão é D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

A função de comparação. O teste de estêncil do CCW passa se a função de estêncil ((ref & Mask) (estêncil & Mask)) é **verdadeira**. Os valores são do tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) . O valor padrão é D3DCMP \_ Always.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Valores de ColorWriteEnable adicionais para os dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo. O valor padrão é 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Valores de ColorWriteEnable adicionais para os dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo. O valor padrão é 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Valores de ColorWriteEnable adicionais para os dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Essa funcionalidade estará disponível se o \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS Capabilities estiver definido no membro PrimitiveMiscCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para o dispositivo. O valor padrão é 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR usado**](d3dcolor.md) para um blend-factor constante durante a combinação alfa. Essa funcionalidade estará disponível se o bit de funcionalidades BLENDFACTOR D3DPBLENDCAPS estiver definido no membro \_ SrcBlendCaps [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou no membro DestBlendCaps **de D3DCAPS9**. Consulte [**D3DRENDERSTATETYPE**](). O valor padrão é 0xffffffff.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Habilita gravações de destino de renderização a serem corrigidas gama para sRGB. O formato deve expor D3DUSAGE \_ SRGBWRITE. O valor padrão é 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Um valor de ponto flutuante que é usado para comparação de valores de profundidade. Consulte [Desvio de profundidade (Direct3D 9)](depth-bias.md). O valor padrão é 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**True** habilita o modo de mesclagem separado para o canal alfa. O valor padrão é **FALSE**.

Quando definido como **false**, os fatores de mesclagem de destino de renderização e as operações aplicadas a Alfa são forçadas a serem as mesmas que as definidas para a cor. Esse modo é efetivamente fisicamente ligado a **false** nas implementações que não definem a Cap D3DPMISCCAPS \_ SEPARATEALPHABLEND. Consulte [D3DPMISCCAPS](d3dpmisccaps.md).

O tipo de mistura alfa separada é determinado pelos \_ Estados de RENDERIZAÇÃO D3DRS SRCBLENDALPHA e \_ D3DRS DESTBLENDALPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) . Esse valor é ignorado, a menos que D3DRS \_ SEPARATEALPHABLENDENABLE seja **true**. O valor padrão é D3DBLEND \_ One.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

Um membro do tipo enumerado [**D3DBLEND**](./d3dblend.md) . Esse valor é ignorado, a menos que D3DRS \_ SEPARATEALPHABLENDENABLE seja **true**. O valor padrão é D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Valor usado para selecionar a operação aritmética aplicada à combinação alfa separada quando o estado de renderização, D3DRS \_ SEPARATEALPHABLENDENABLE, é definido como **TRUE.**

Os valores válidos são definidos pelo tipo enumerado [**D3DBLENDOP.**](./d3dblendop.md) O valor padrão é D3DBLENDOP \_ ADD.

Se a funcionalidade do dispositivo BLENDOP D3DPMISCCAPS não tiver \_ suporte, D3DBLENDOP \_ ADD será executada. Consulte [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários



| Renderizar estados        |   Amostra de textura                 |
|----------------------|--------------------|
| ps \_ 1 \_ 1 a ps \_ 1 \_ 3 | 4 amostras de textura |



 

O Direct3D define a constante D3DRENDERSTATE WRAPBIAS como uma conveniência para que os aplicativos habilitam ou desabilitem a quebra de textura, com base no inteiro baseado em zero de um conjunto de coordenadas de textura (em vez de usar explicitamente um dos valores de estado \_ D3DRS \_ WRAP n). Adicione o valor D3DRENDERSTATE WRAPBIAS ao índice baseado em zero de um conjunto de coordenadas de textura para calcular o valor D3DRS WRAP n que corresponde a esse índice, conforme mostrado no exemplo \_ a \_ seguir.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
