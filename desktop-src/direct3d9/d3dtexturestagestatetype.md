---
description: Estados de estágio de textura definem operações de textura de vários blender.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumeração D3DTEXTURESTAGESTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4879009f603a6943302f0595f37176ec5edf8e1a1d3212efedb66c923d775104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894146"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Enumeração D3DTEXTURESTAGESTATETYPE

Estados de estágio de textura definem operações de textura de vários blender. Alguns estados de exemplo configuram o processamento de vértice e outros configuram o processamento de pixel. Os estados do estágio de textura podem ser salvos e restaurados usando stateblocks (consulte Estado de salvar e restaurar blocos de estado [(Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

O estado do estágio de textura é uma operação de mesclagem de cores de textura identificada por um membro do tipo enumerado [**D3DTEXTUREOP.**](./d3dtextureop.md) O valor padrão para o primeiro estágio de textura (estágio 0) é D3DTOP MODULARTE; para todos os outros estágios, o padrão \_ é D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

O estado do estágio de textura é o primeiro argumento de cor para o estágio, identificado por um dos [D3DTA.](d3dta.md) O argumento padrão é TEXTURE D3DTA. \_

Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

O estado do estágio de textura é o segundo argumento de cor para o estágio, identificado por [D3DTA.](d3dta.md) O argumento padrão é D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O valor padrão para o registro é (0.0, 0.0, 0.0, 0.0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

O estado do estágio de textura é uma operação de mesclagem alfa de textura identificada por um membro do tipo enumerado [**D3DTEXTUREOP.**](./d3dtextureop.md) O valor padrão para o primeiro estágio de textura (estágio 0) é D3DTOP SELECTARG1 e, para todos os outros estágios, o padrão \_ é D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

O estado do estágio de textura é o primeiro argumento alfa para o estágio, identificado por [D3DTA.](d3dta.md) O argumento padrão é TEXTURE D3DTA. \_ Se nenhuma textura for definida para esse estágio, o argumento padrão será D3DTA \_ DIFUSO. Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**ALFAARG2 D3DTSS \_**
</dt> <dd>

O estado do estágio de textura é o segundo argumento alfa para o estágio, identificado por [D3DTA.](d3dta.md) O argumento padrão é D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

O estado do estágio de textura é um valor de ponto flutuante para \[ o coeficiente \] \[ 0 0 \] em uma matriz de mapeamento de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

O estado do estágio de textura é um valor de ponto flutuante para o coeficiente \[ \] \[ 0 1 \] em uma matriz de mapeamento de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

O estado do estágio de textura é um valor de ponto flutuante para \[ o coeficiente \] \[ 1 0 \] em uma matriz de mapeamento de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

O estado do estágio de textura é um valor de ponto flutuante para \[ o coeficiente \] \[ 1 1 \] em uma matriz de mapeamento de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Índice do conjunto de coordenadas de textura a ser usado com esse estágio de textura. Você pode especificar até oito conjuntos de coordenadas de textura por vértice. Se um vértice não incluir um conjunto de coordenadas de textura no índice especificado, o sistema assume como padrão as coordenadas você e v (0,0).

Ao renderizar usando sombreadores de vértice, o índice de coordenadas de textura de cada estágio deve ser definido como seu valor padrão. O índice padrão para cada estágio é igual ao índice de estágio. De definir esse estado como o índice baseado em zero do conjunto de coordenadas para cada vértice que esse estágio de textura usa.

Além disso, os aplicativos podem incluir, como OR lógico com o índice sendo definido, uma das constantes para solicitar que o Direct3D gere automaticamente as coordenadas de textura de entrada para uma transformação de textura. Para ver uma lista de todas as constantes, consulte [D3DTSS \_ TCI](d3dtss-tci.md).

Com exceção de D3DTSS \_ TCI PASSTHRU, que resolve para zero, se qualquer um dos valores a seguir estiver incluído com o índice sendo definido, o sistema usará o índice estritamente para determinar o modo de quebra de \_ textura. Esses sinalizadores são mais úteis ao executar o mapeamento de ambiente.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Valor de escala de ponto flutuante para luminância do mapa de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

Valor de deslocamento de ponto flutuante para luminância do mapa de elevações. O valor padrão é 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**TEXTURA \_ D3DTSSTRANSFORMFLAGS**
</dt> <dd>

Membro do tipo [**enumerado D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) que controla a transformação de coordenadas de textura para esse estágio de textura. O valor padrão é D3DTTFF \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Configurações para o terceiro operador de cor para operações anármicas (multiplicar, adicionar e interpolar linearmente), identificado por [D3DTA](d3dta.md). Essa configuração será suportada se as funcionalidades do dispositivo LERP D3DTEXOPCAPS \_ MULTIPLYADD ou D3DTEXOPCAPS \_ estão presentes. O argumento padrão é D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O valor padrão para o registro é (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**ALFAARG0 D3DTSS \_**
</dt> <dd>

Configurações para o operador do seletor de canal alfa para operações anármicas (multiplicar, adicionar e interpolar linearmente), identificado por [D3DTA](d3dta.md). Essa configuração será suportada se as funcionalidades do dispositivo LERP D3DTEXOPCAPS \_ MULTIPLYADD ou D3DTEXOPCAPS \_ estão presentes. O argumento padrão é D3DTA \_ CURRENT. Especifique D3DTA \_ TEMP para selecionar uma cor de registro temporário para leitura ou gravação. Há suporte para D3DTA TEMP se a funcionalidade do dispositivo \_ \_ TSSARGTEMP D3DPMISCCAPS estiver presente. O argumento padrão é (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Configuração para selecionar o registro de destino para o resultado deste estágio, identificado por [D3DTA](d3dta.md). Esse valor pode ser definido como D3DTA CURRENT (o valor padrão) ou como TEMP D3DTA, que é um único registro temporário que pode ser lido em estágios subsequentes como um argumento \_ \_ de entrada. A cor final passada para o blender de liquidificador e o buffer de quadro é retirada do D3DTA CURRENT, portanto, o último estado do estágio de textura ativo deve ser definido para \_ gravar como atual. Essa configuração será suportada se a funcionalidade do dispositivo \_ TSSARGTEMP D3DPMISCCAPS estiver presente.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**CONSTANTE D3DTSS \_**
</dt> <dd>

Cor da constante por estágio. Para ver se um dispositivo dá suporte a uma cor constante por estágio, consulte a constante D3DPMISCCAPS \_ PERSTAGECONSTANT [em D3DPMISCCAPS](d3dpmisccaps.md). A CONSTANTE D3DTSS \_ é usada pela CONSTANTE D3DTA. \_ Consulte [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros desse tipo enumerado são usados com os métodos [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para recuperar e definir valores de estado de textura.

O intervalo válido de valores para os coeficientes de matriz de mapeamento de aumento \_ DE BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 e D3DTSS BUMPENVMAT11 é maior ou igual a -8,0 e menor que \_ 8,0. Esse intervalo, expresso em notação matemática é (-8.0,8.0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
