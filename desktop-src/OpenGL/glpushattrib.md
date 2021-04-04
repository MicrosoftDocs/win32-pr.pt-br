---
title: função glPushAttrib (GL. h)
description: Envia a pilha de atributos por push.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- função glPushAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009051"
---
# <a name="glpushattrib-function"></a>função glPushAttrib

Envia a pilha de atributos por push.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mascara* 
</dt> <dd>

Uma máscara que indica quais atributos salvar. As constantes de máscara simbólica e seu estado de OpenGL associado são os seguintes (os parágrafos recuados listam os atributos que são salvos):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>BIT de buffer do GL \_ Accum \_ \_ 
</dt> <dd>

Valor de limpeza do buffer de acumulação

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit do \_ buffer de cores GL \_
</dt> <dd>

\_Bit de \_ habilitação de teste do GL alfa

Função de teste alfa e valor de referência

\_Bit de habilitação do GL Blend

Combinando funções de origem e de destino

\_Bit de habilitação de pontilhamento GL

Configuração do buffer de \_ desenho GL \_

\_Bit de \_ habilitação de op lógico GL

Função op lógica

Valores claros de modo de cor e de modo de índice

Modo de cor e writemasks de modo de índice

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>BIT do GL \_ atual \_
</dt> <dd>

Cor RGBA atual

Índice de cores atual

Vetor normal atual

Coordenadas de textura atuais

\_ \_ \_ Sinalizador válido de posição de \_ rasterização atual de posição de varredura atual

Cor RGBA associada à posição de rasterização atual

Índice de cores associado à posição de rasterização atual

Coordenadas de textura associadas à posição de rasterização atual

Sinalizador de sinalizador de \_ borda GL \_

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ buffer de profundidade GL \_
</dt> <dd>

\_Bit de \_ habilitação de teste de profundidade GL

Função de teste do buffer de profundidade

Valor de limpeza do buffer de profundidade

\_Bit GL \_ WRITEMASK de habilitação de profundidade

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit de habilitação GL \_
</dt> <dd>

\_Sinalizador de teste alfa do GL \_

\_Sinalizador normal automático do GL \_

\_Sinalizador de combinação GL

Habilitar bits para os planos de recorte definíveis pelo usuário

\_material de cor GL \_

Sinalizador de face de \_ seleção GL \_

Sinalizador de teste de \_ profundidade GL \_

\_Sinalizador de pontilhamento GL

\_Sinalizador de neblina GL

GL \_ Light *i* em que 0 <= *i* < GL \_ Max \_ luzes

\_Sinalizador de iluminação GL

\_Sinalizador Smooth de linha gl \_

Sinalizador de STIPPLE de \_ linha gl \_

\_Sinalizador de \_ op da lógica de cores GL \_

\_Sinalizador de \_ op lógico de índice GL \_

GL \_ MAP1 \_ x, em que x é um tipo de mapa

GL \_ map2 \_ x, em que x é um tipo de mapa

\_Sinalizador de NORMALIZE GL

\_Sinalizador suave de ponto GL \_

\_Sinalizador de \_ linha de deslocamento do polígono GL \_

\_Sinalizador de \_ preenchimento de deslocamento do polígono GL \_

\_Sinalizador de \_ ponto de deslocamento do polígono GL \_

\_Sinalizador suave do polígono GL \_

\_Sinalizador STIPPLE de polígono GL \_

Sinalizador de teste de \_ tesoura GL \_

Sinalizador de teste do \_ estêncil GL \_

Sinalizador de 1D de \_ textura GL \_

\_Sinalizador de textura 2D do GL \_

Sinalizadores GL \_ Texture \_ Gen \_ x em que x é S, T, R ou Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit de avaliação GL \_
</dt> <dd>

GL \_ MAP1 \_ x habilitar bits, em que x é um tipo de mapa

GL \_ map2 \_ x habilitar bits, em que x é um tipo de mapa

pontos de extremidade de grade 1-D e divisões

pontos de extremidade de grade 2D e divisões

\_Bit de \_ habilitação normal automática do GL

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de neblina GL \_
</dt> <dd>

\_Sinalizador de habilitação de neblina do GL

Cor da neblina

Densidade de neblina

Início da neblina linear

Fim da neblina linear

Índice de neblina

Valor do modo de \_ neblina do GL \_

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit de dica GL \_
</dt> <dd>

\_Configuração da \_ dica de correção de perspectiva GL \_

\_Configuração de \_ dica simples do ponto GL \_

\_Configuração de \_ dica Smooth de linha gl \_

\_Configuração de \_ \_ dica do Polygon do GL

Configuração de dica de \_ neblina do GL \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit de iluminação GL \_
</dt> <dd>

\_Bit de \_ habilitação do material de cor GL

\_Valor de \_ face do material de cor GL \_

Parâmetros de material de cor que estão acompanhando a cor atual

Cor da cena ambiente

\_Valor do \_ \_ Visualizador local do modelo Light GL \_

\_ \_ \_ \_ Configuração do lado do modelo Light GL dois lados

\_Bit de habilitação de iluminação GL

Habilitar bit para cada luz

Intensidade de ambiente, difuso e especular para cada luz

Direção, posição, expoente e ângulo de corte para cada luz

Fatores de atenuação constantes, lineares e quadráticas para cada luz

Cor de ambiente, difuso, especular e emissiva para cada material

Índices de cores de ambiente, difuso e especulares para cada material

Expoente especular para cada configuração de modelo de \_ tonalidade de material GL \_

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de linha gl \_ 
</dt> <dd>

\_Sinalizador Smooth de linha gl \_

\_STIPPLE de linha gl \_ habilitar bit

Padrão de Stipple de linha e contador de repetição

Largura da linha

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit da lista GL \_
</dt> <dd>

Configuração da base da \_ lista GL \_

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit do \_ modo de pixel GL \_
</dt> <dd>

\_Configurações de escala do GL vermelho \_ e GL em \_ vermelho \_

\_ \_ Valores de escala GL verde e GL \_ verde \_

\_Diferença azul do GL \_ e \_ escala azul do GL \_

\_ \_ Escala de alfa de polarização alfa e GL \_ \_

\_ \_ Escala de profundidade de nível GL e GL \_ \_

\_ \_ Valores de deslocamento do índice GL e do \_ índice GL \_

\_ \_ Sinalizadores de estêncil de mapa de cores e de \_ mapas GL GL \_

GL \_ \_ de zoom X e GL- \_ \_ fatores Y de zoom

Configuração do buffer de \_ leitura GL \_

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de ponto GL \_
</dt> <dd>

\_Sinalizador suave de ponto GL \_

Tamanho do ponto

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit do polígono GL \_
</dt> <dd>

\_Bit de \_ habilitação de face de seleção GL

\_Valor do modo de seleção de \_ face GL \_

\_Indicador de front face do GL \_

Configuração do modo de \_ polígono GL \_

\_Sinalizador suave do polígono GL \_

\_STIPPLE Polygon GL \_ bit de habilitação

\_Sinalizador de \_ preenchimento de deslocamento do polígono GL \_

\_Sinalizador de \_ linha de deslocamento do polígono GL \_

\_Sinalizador de \_ ponto de deslocamento do polígono GL \_

\_fator de \_ deslocamento do polígono GL \_

\_unidades de \_ deslocamento do polígono GL \_

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_STIPPLE de polígono do GL \_ \_
</dt> <dd>

Imagem de Stipple do polígono

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>BIT GL de \_ tesoura \_
</dt> <dd>

Sinalizador de teste de \_ tesoura GL \_

Caixa de tesoura

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ buffer do estêncil GL \_
</dt> <dd>

\_Bit de \_ habilitação de teste do estêncil GL

Função de estêncil e valor de referência

Máscara de valor do estêncil

Ações de passagem de buffer de falha, passagem e profundidade do estêncil

Valor de limpeza do buffer do estêncil

Writemask do buffer de estêncil

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de textura GL \_
</dt> <dd>

Habilitar bits para as quatro coordenadas de textura

Cor da borda de cada imagem de textura

Função minificação para cada imagem de textura

Função de ampliação para cada imagem de textura

Coordenadas de textura e modo de encapsulamento para cada imagem de textura

Cor e modo para cada ambiente de textura

Habilitar o bits GL \_ Texture \_ Gen \_ *x*; *x* é S, T, R e Q

\_ \_ \_ Configuração do modo do GL Texture Gen para S, T, R e Q

equações do plano glTexGen para S, T, R e Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformação GL \_
</dt> <dd>

Coeficientes dos seis planos de recorte

Habilitar bits para os planos de recorte definíveis pelo usuário

Valor do modo de \_ matriz GL \_

\_Sinalizador de NORMALIZE GL

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit GL viewport \_
</dt> <dd>

Intervalo de profundidade (próximo e longe)

Origem e extensão do visor

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_estouro de pilha GL \_**</dt> </dl>    | A função foi chamada enquanto a pilha de atributos estava cheia.<br/>                                                                |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPushAttrib** usa um argumento, uma máscara que indica quais grupos de variáveis de estado salvar na pilha de atributos. As constantes simbólicas são usadas para definir os bits na máscara. O parâmetro Mask normalmente é construído aplicando-se a operação **or** lógica a várias dessas constantes. Você pode usar a máscara especial GL \_ todos \_ os \_ bits de Atrib para salvar todos os Estados empilháveis.

A função [**glPopAttrib**](glpopattrib.md) restaura os valores das variáveis de estado salvas com o último comando **glPushAttrib** . Aqueles não salvos são deixados inalterados.

É um erro enviar atributos por push para uma pilha completa ou para os atributos pop de uma pilha vazia. Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.

Inicialmente, a pilha de atributos está vazia.

Nem todos os valores para o estado OpenGL podem ser salvos na pilha de atributos. Por exemplo, você não pode salvar o pacote de pixel e o estado de desempacotamento, estado do modo de renderização e estado de seleção e comentários.

A profundidade da pilha de atributos depende da implementação, mas deve ser pelo menos 16.

As funções a seguir recuperam informações relacionadas a **glPushAttrib** e [**glPopAttrib**](glpopattrib.md):

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de Atrib glGet com Argument GL \_ \_ \_

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ ATRIB \_ glGet com Argument GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





