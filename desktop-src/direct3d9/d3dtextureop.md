---
description: Define operações de mesclagem de textura por estágio.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumeração D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298552"
---
# <a name="d3dtextureop-enumeration"></a>Enumeração D3DTEXTUREOP

Define operações de mesclagem de textura por estágio.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ desabilitar**
</dt> <dd>

Desabilita a saída deste estágio de textura e todos os estágios com um índice mais alto. Para desabilitar o mapeamento de textura, defina como a operação de cor para o primeiro estágio de textura (estágio 0). As operações alfa não podem ser desabilitadas quando as operações de cores estão habilitadas. Definir a operação Alpha como D3DTOP \_ Disable quando a mesclagem de cores está habilitada causa um comportamento indefinido.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Use a primeira cor ou argumento alfa do estágio de textura, sem modificações, como a saída. Essa operação afeta o argumento de cor quando usado com o \_ estado de D3DTSS COLOROP de textura e o argumento alfa quando usado com D3DTSS \_ ALPHAOP.

![equação deste argumento (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Use a segunda cor ou o argumento alfa do estágio de textura, sem modificações, como a saída. Essa operação afeta o argumento de cor quando usado com o \_ estado de estágio de textura D3DTSS COLOROP e o argumento alfa quando usado com D3DTSS \_ ALPHAOP.

![equação deste argumento (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modular D3DTOP**
</dt> <dd>

Multiplique os componentes dos argumentos.

![equação da operação modular (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

Multiplique os componentes dos argumentos e SHIFTe os produtos para a esquerda 1 bit (efetivamente multiplicando-os por 2) para clareamento.

![equação da operação Modulate2X (s (RGBA) = (arg1 x ARG 2) e, em seguida, SHIFT esquerda 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

Multiplique os componentes dos argumentos e mude os produtos para os 2 bits à esquerda (com eficiência, multiplique-os por 4) para clarear.

![equação da operação Modulate4X (s (RGBA) = (arg1 x ARG 2) e, em seguida, SHIFT esquerda 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Adicionar**
</dt> <dd>

Adicione os componentes dos argumentos.

![equação da operação de adição (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDsigned**
</dt> <dd>

Adicione os componentes dos argumentos com uma diferença de a-0,5, tornando o intervalo de valores efetivo de-0,5 até 0,5.

![equação da operação Adicionar assinada (s (RGBA) = arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Adicione os componentes dos argumentos com uma tendência de a-0,5 e SHIFTe os produtos para a esquerda 1 bit.

![equação do Adicionar operação 2x assinada ((s (RGBA) = arg1 + ARG 2-0,5) e, em seguida, SHIFT esquerda 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Subtrair D3DTOP**
</dt> <dd>

Subtraia os componentes do segundo argumento daqueles do primeiro argumento.

![equação da operação de subtração (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDsmooth**
</dt> <dd>

Adicionar o primeiro e o segundo argumentos; em seguida, subtraia seu produto da soma.

![equação da operação Adicionar suave (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**
</dt> <dd>

Mescle linearmente esse estágio de textura, usando o alfa interpolado de cada vértice.

![equação da operação alfa difusa do Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**
</dt> <dd>

Mescle linearmente este estágio de textura, usando o alfa da textura deste estágio.

![equação da operação alfa de textura de mesclagem (s (RGBA) = arg1 x alfa + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**
</dt> <dd>

Mescle linearmente esse estágio de textura, usando um conjunto de Alpha escalar com o \_ estado de RENDERIZAÇÃO D3DRS TEXTUREFACTOR.

![equação da operação alfa do fator de mistura (s (RGBA) = arg1 x alfa + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**
</dt> <dd>

Misturar linearmente um estágio de textura que usa um alfa previamente multiplicado.

![equação da operação do Blend Texture Alpha PM (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**
</dt> <dd>

Mescle linearmente este estágio de textura, usando alfa tirado do estágio de textura anterior.

![equação da operação alfa (s (RGBA) atual de Blend = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREmodular**
</dt> <dd>

D3DTOP \_ PREmodular está definido no estágio n. A saída do estágio n é arg1. Além disso, se houver uma textura no estágio n + 1, qualquer D3DTA \_ atual no estágio n + 1 será contramultiplicado por textura no estágio n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**Addcolor D3DTOP \_ MODULATEALPHA \_**
</dt> <dd>

Modular a cor do segundo argumento, usando o alfa do primeiro argumento; em seguida, adicione o resultado ao argumento um. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

![equação da operação Adicionar alfa modular de cor (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ addalpha**
</dt> <dd>

Modular os argumentos; em seguida, adicione o alfa do primeiro argumento. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

![equação da operação de adição de cor de alfa modular (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**Addcolor D3DTOP \_ MODULATEINVALPHA \_**
</dt> <dd>

Semelhante a D3DTOP \_ MODULATEALPHA \_ addcolor, mas use o inverso do alfa do primeiro argumento. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

![equação da operação de adição de alfa inversa (s (RGBA) de modulação de cor = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ addalpha**
</dt> <dd>

Semelhante a D3DTOP \_ MODULATECOLOR \_ addalpha, mas use o inverso da cor do primeiro argumento. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

![equação da operação de adição de cor inversa alfa modular (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**
</dt> <dd>

Execute o mapeamento de relevo por pixel, usando o mapa de ambiente no próximo estágio de textura, sem luminância. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**
</dt> <dd>

Execute o mapeamento de relevo por pixel, usando o mapa de ambiente no próximo estágio de textura, com luminância. Esta operação só tem suporte para operações de cor (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Modular os componentes de cada argumento como componentes assinados, adicionar seus produtos; em seguida, replique a soma para todos os canais de cores, incluindo alfa. Esta operação tem suporte para operações de cor e alfa.

![equação da operação do ponto 3 do produto (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

No DirectX 6 e DirectX 7, as operações de multitexturas as entradas acima são todas deslocadas pela metade (y = x-0,5) antes de usar para simular dados assinados, e o resultado escalar é automaticamente clamped para valores positivos e replicados para todos os três canais de saída. Além disso, observe que, como uma operação de cor, isso não atualizou o alfa que apenas atualiza os componentes RGB.

No entanto, em sombreadores do DirectX 8,1, você pode especificar que a saída seja roteada para os componentes. RGB ou. a ou ambos (o padrão). Você também pode especificar uma operação escalar separada no canal alfa.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**
</dt> <dd>

Executa uma operação de acumulação de multiplicação. Ele usa os dois últimos argumentos, multiplica-os juntos e os adiciona ao argumento restante de entrada/origem e coloca isso no resultado.

S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**
</dt> <dd>

Interpola linearmente entre o segundo e o terceiro argumentos de origem por uma proporção especificada no primeiro argumento de origem.

S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* Arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros desse tipo são usados ao definir operações de cor ou alfa usando os valores de D3DTSS \_ COLOROP ou D3DTSS \_ ALPHAOP com o método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .

Nas fórmulas acima, S<sub>RGBA</sub> é a cor RGBA produzida por uma operação de textura e arg1, arg2 e Arg3 representam a cor de RGBA completa dos argumentos de textura. Componentes individuais de um argumento são mostrados com subscritos. Por exemplo, o componente alfa para o argumento 1 seria mostrado como arg1<sub>A</sub>.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
