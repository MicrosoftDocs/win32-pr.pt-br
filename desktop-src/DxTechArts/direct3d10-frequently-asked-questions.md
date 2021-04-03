---
title: 10 perguntas frequentes sobre o Direct3D
description: Este artigo contém algumas das perguntas frequentes sobre o Direct3D 10 a partir do ponto de vista de um desenvolvedor que está portando um aplicativo existente do Direct3D 9 (D3D9) para o Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084672"
---
# <a name="direct3d-10-frequently-asked-questions"></a>10 perguntas frequentes sobre o Direct3D

Este artigo contém algumas das perguntas frequentes sobre o Direct3D 10 a partir do ponto de vista de um desenvolvedor que está portando um aplicativo existente do Direct3D 9 (D3D9) para o Direct3D 10 (D3D10).

-   [Buffers de constantes](#constant-buffers)
-   [State](#state)
-   [Formatos](#formats)
-   [Vinculação de sombreador](#shader-linkage)
-   [Chamar chamadas](#draw-calls)
-   [Recursos](#resources)
-   [Profundidade como textura](#depth-as-texture)
-   [MSAA](#msaa)
-   [Falhas](#crashes)
-   [Renderização de predicado](#predicated-rendering)
-   [Sombreador de geometria](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Buffers de constantes

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Qual é a melhor maneira de atualizar os buffers de constantes?
</dt> <dd>

UpdateSubresource e MAP com descarte devem ter aproximadamente a mesma velocidade. Escolha entre elas, dependendo de qual delas copia a quantidade mínima de memória. Se você já tiver seus dados armazenados na memória em um bloco contíguo, use UpdateSubresource. Se você precisar acumular dados de outros locais, use mapear com descartar.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Qual é a pior maneira de organizar os buffers de constantes?
</dt> <dd>

O pior desempenho é realizado ao colocar todas as constantes para um sombreador específico em um buffer constante. Embora isso geralmente seja a maneira mais fácil de portar de D3D9 para D3D10, ele pode prejudicar o desempenho. Por exemplo, considere um cenário que usa o seguinte buffer de constantes:

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

O buffer é de 6560 bytes. Suponha que haja um aplicativo com 1000 objetos a serem processados, 100 dos quais são malhas com revestimento e 900 das que são malhas estáticas. Além disso, suponha que esse aplicativo esteja usando o mapeamento de sombra com uma fonte de luz. Isso significa que há duas passagens, uma para o mapa de profundidade renderizado da luz e outra para a passagem de renderização de encaminhamento. Isso resulta em chamadas de empate de 2000. Embora cada chamada de desenho não precise atualizar todas as partes do buffer de constantes, todo o buffer de constante ainda é atualizado e enviado para o cartão. Isso resulta na atualização de 13 MB de dados a cada quadro (o 2000 Draw chama o tempo de 6560 KB).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Qual é a melhor maneira de organizar meus buffers de constantes?
</dt> <dd>

A melhor maneira é organizar buffers constantes por frequência de atualização. As constantes que são atualizadas em frequências semelhantes devem estar no mesmo buffer. Por exemplo, considere o cenário apresentado em "Qual é a pior maneira de organizar buffers de constantes?", mas com um layout de constante melhor:

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

Os buffers de constantes são divididos por sua frequência de atualização, mas isso só é metade da solução. O aplicativo precisa atualizar os buffers de constantes corretamente para tirar total proveito da divisão. Vamos pressupor a mesma cena acima: 900 malhas estáticas, 100 malhas com revestimento, uma passagem leve e uma passagem de avanço. Também presumiremos que alguns buffers de constante por objeto serão armazenados. Isso significa que cada objeto conterá um VSPerSkinnedCB ou um VSPerStaticCB, dependendo se ele é ou não docapado ou estático. Fazemos isso para evitar o dobro da quantidade de matrizes enviadas por meio do pipeline.

Dividimos o quadro em três fases. A primeira fase é o início do quadro e não envolve nenhuma renderização, apenas atualizações constantes.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Iniciar quadro**
</dt> <dd>

-   Atualizar VSGlobalPerFrameCB para o tempo do aplicativo (4 bytes)
-   Atualizar a 100 VSPerSkinnedCB para os objetos 100 com revestimento (640000 bytes)
-   Atualizar VSPerStaticCB para objetos estáticos 900 (57600 bytes)

A seguir está a passagem do mapa de sombra. Observe que o único buffer constante que realmente atualiza é VSPerPassCB. Todos os outros buffers de constantes foram atualizados durante a fase de início do quadro. Embora ainda precisemos associar esses buffers de constantes, a quantidade de informações passadas para a placa de vídeo é mínima, porque os buffers já foram atualizados.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passagem de sombra**
</dt> <dd>

-   Atualizar VSPerPassCB (72 bytes)
-   Empates 100 malhas com revestimento (100 associações, sem atualizações)
-   Desenhe malhas estáticas 900 (100 associações, sem atualizações)

Da mesma forma, a passagem de renderização de encaminhamento só precisa atualizar dados por material, pois ela não foi armazenada por malha. Se presumirmos que há 500 materiais em uso na cena:

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Passagem de encaminhamento**
</dt> <dd>

-   Atualizar VSPerPassCB (72 bytes)
-   Atualização 500 VSPerMaterialCBs (10000 bytes)

Isso resulta em um total de apenas 707 KB. Embora esse seja um cenário muito forçado, ele ilustra a quantidade de sobrecarga de atualização constante que pode ser reduzida por meio da classificação de constantes por frequência de atualização.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>E se eu não tiver espaço suficiente para armazenar buffers de constantes individuais para minhas malhas, material e assim por diante? 
</dt> <dd>

Você sempre pode usar um sistema em camadas de buffers de constantes. Crie buffers de constante de tamanho variável (16 bytes, 32 bytes, 64 bytes e assim por diante) até o maior tamanho de buffer constante necessário. Quando for o momento de associar um buffer constante a um sombreador, selecione o menor buffer de constante que pode conter os dados necessários para o sombreador. Embora essa abordagem seja um pouco menos eficiente, ela é uma boa etapa intermediária.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Estou compartilhando buffers de constantes entre diferentes sombreadores. Um sombreador pode usar todas as constantes, mas outra pode usar algumas das constantes. Qual é a melhor maneira de atualizá-los? 
</dt> <dd>

Uma abordagem é dividir ainda mais o buffer constante. No entanto, há um ponto em que muitos buffers de constante estão associados. Nesse caso, mova as constantes que provavelmente não serão usadas por vários sombreadores no final do buffer de constantes. Ao obter os dados de variável do sombreador, use o \_ sinalizador d3d10 SVF \_ used da \_ variável de sombreador d3d10 \_ \_ desc para determinar se a variável é usada. Ao colocar variáveis não utilizadas no final do buffer de constantes, você pode associar um buffer menor ao sombreador que não usa essas variáveis, poupando assim o custo de atualização.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Quanto posso melhorar minha taxa de quadros se eu carregar apenas os Bones do meu caractere uma vez por quadro, em vez de uma vez por passagem/desenho? 
</dt> <dd>

Você pode melhorar a taxa de quadros entre 8% e 50 por cento, dependendo da quantidade de dados redundantes. No pior caso, o desempenho não será reduzido.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Quantos buffers de constantes devo associar ao mesmo tempo? 
</dt> <dd>

Associe o número mínimo de buffers de constante que é necessário para obter todos os dados no sombreador. Em um cenário realista, cinco é o número recomendado de buffers de constantes a serem usados. O compartilhamento de buffers de constantes entre sombreadores (ligando o mesmo CB para o VS e PS) também pode melhorar o desempenho.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Há um custo para ligar buffers constantes sem usá-los? 
</dt> <dd>

Sim, se você não for realmente usar o buffer, não chame VSSetConsantBuffer ou PSSetConstantBuffer. Essa sobrecarga extra da API pode ser somada ao longo de várias chamadas de desenho.

</dd> </dl>

## <a name="state"></a>Estado

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Qual é a melhor maneira de gerenciar o estado no D3D10? 
</dt> <dd>

A melhor solução é conhecer todo o seu estado de antecedência e criar os objetos de estado antecipadamente. Isso significa que, no momento do processamento, a associação de estado é a única operação que precisa acontecer. D3D10 também filtra duplicatas.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Meu jogo carregou dinamicamente ou tem conteúdo gerado pelo usuário. Não consigo carregar todos os meus objetos de estado antecipadamente. O que devo fazer? 
</dt> <dd>

Há duas soluções aqui. A primeira é apenas criar objetos de estado imediatamente e permitir que o D3D10 filtre duplicatas. No entanto, isso não é recomendado para cenários com muitas alterações de objeto de estado por quadro. Uma solução melhor é fazer o hash dos objetos de estado por conta própria e criar um objeto de estado somente se um que se ajuste aos requisitos não for encontrado na tabela de hash. O raciocínio por trás do uso de uma tabela de hash personalizada é que um aplicativo pode selecionar um hash rápido com base no cenário de uso específico para esse aplicativo. Por exemplo, se um aplicativo altera apenas o rendertargetwritemask no Blendstate e mantém todos os outros valores iguais, o aplicativo pode gerar um hash do rendertargetwritemask em vez de toda a estrutura.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>O estado AlphaTest não existe mais. Onde foi? 
</dt> <dd>

AlphaTest agora deve ser o desempenho no sombreador. Consulte o exemplo de FixedFuncEMU.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>O que aconteceu com os planos de clipes do usuário? 
</dt> <dd>

Os planos de clipes do usuário foram movidos para o sombreador. Há duas maneiras de lidar com isso. A primeira é a saída de \_ ClipDistance de VA do sombreador de vértice ou do sombreador de geometria. A outra opção é usar o descarte no sombreador de pixel com base em um valor passado pelo sombreador de vértice ou pelo sombreador Geometry. Experimente ambos para ver qual é mais rápido para seu cenário específico. O uso de \_ ClipDistance de VA pode fazer com que o hardware use uma rotina de recorte baseada em geometria que pode fazer com que as chamadas de empate de limite de geometria sejam executadas mais lentamente. Da mesma forma, o uso de descarte desloca o trabalho para o sombreador de pixel, o que pode fazer com que as chamadas de empate com limite de pixel sejam executadas mais lentamente.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Desmarcações não respeitam nenhuma configuração de estado, como minhas configurações de Rect de tesoura no estado do rasterizador. 
</dt> <dd>

As desmarcações foram separadas do estado do pipeline. Para obter o comportamento do estilo D3D9, emular limpas desenhando um quatro de tela inteira.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Defini meus Estados de volta para o padrão para tentar diagnosticar um erro de renderização. Agora, minha tela mostra apenas preto, embora eu saiba que estou desenhando objetos na tela. 
</dt> <dd>

Ao definir o estado de volta para valores padrão (NULL), verifique se SampleMask na chamada para OMSetBlendState nunca é zero. Se SampleMask for definido como zero, então todos os exemplos serão logicamente e com zero. Nesse cenário, nenhum exemplo passará no teste de mistura.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Para onde o estado do D3DSAMP \_ SRGBTEXTURE é usado? 
</dt> <dd>

O SRGB foi removido como parte do estado de amostra e agora está vinculado ao formato de textura. A associação de uma textura SRGB resultará na mesma amostragem que você obteria se tiver especificado D3DSAMP \_ SRGBTEXTURE no Direct3D 9.

</dd> </dl>

## <a name="formats"></a>Formatos

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Qual formato D3D9 corresponde ao formato D3D10? 
</dt> <dd>

Para obter informações, consulte [considerações do Direct3D 9 para o Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>O que aconteceu com os formatos de textura A8R8G8B8? 
</dt> <dd>

Eles foram preteridos no D3D10. Você pode recriar suas texturas como R8G8B8A8, ou pode swizzle-las na carga ou pode swizzle no sombreador.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Como fazer usar texturas palettized? 
</dt> <dd>

Coloque a paleta de cores em uma textura ou em um buffer de constantes e associe-a ao pipeline. No sombreador de pixel, faça uma pesquisa indireta usando o índice em sua textura palettized.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quais são esses novos formatos SRGB? 
</dt> <dd>

O SRGB foi removido como parte do estado de amostra e agora está vinculado ao formato de textura. A associação de uma textura SRGB resultará na mesma amostragem que você obteria se tiver especificado D3DSAMP \_ SRGBTEXTURE no Direct3D 9.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Onde os fãs do triângulo vão? 
</dt> <dd>

Os fãs do triângulo foram preteridos no D3D10. Os fãs do triângulo precisarão ser convertidos no pipeline de conteúdo ou no carregamento.

</dd> </dl>

## <a name="shader-linkage"></a>Vinculação de sombreador

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Meus sombreadores do Direct3D 9 são bem compilados no modelo do sombreador 4,0, mas quando os vinculo ao pipeline, obtenho erros de vinculação aparecendo na saída de depuração com o tempo de execução de depuração. 
</dt> <dd>

O vínculo do sombreador é muito mais estrito em D3D10. Os elementos em um estágio subsequente devem ser lidos na ordem em que são gerados do estágio anterior. Por exemplo:

Saídas de um sombreador de vértice:

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Um sombreador de pixel lê em:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Embora a posição não seja necessária no sombreador de pixel, isso causará um erro de vinculação, pois a posição está sendo saída do sombreador de vértice, mas não lida pelo sombreador de pixel. A versão mais correta ficaria assim:

Saídas de um sombreador de vértice:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Um sombreador de pixel lê em:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Nesse caso, o sombreador de vértice está gerando as mesmas informações, mas agora o sombreador de pixel está lendo as coisas na saída do pedido. Como o sombreador de pixel não está lendo nada após Tex, não precisamos se preocupar que o VS está gerando mais informações do que o PS está lendo.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Preciso de uma assinatura de sombreador para criar um layout de entrada, mas eu carregou minhas malhas e Crio layouts antes de criar sombreadores. O que devo fazer? 
</dt> <dd>

Uma solução é mudar os sombreadores de pedido e de carga antes de carregar malhas. No entanto, isso é muito mais fácil, dito do que fazer. Você sempre pode criar os layouts de entrada sob demanda quando necessário pelo aplicativo. Você precisará manter uma versão da assinatura do sombreador. Você deve criar um hash com base no layout do sombreador e do buffer e apenas criar o layout de entrada se um que corresponda ainda não existir.

</dd> </dl>

## <a name="draw-calls"></a>Chamar chamadas

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Qual é o meu limite para chamadas de desenho para D3D10 alcançar 60 Hz? 30 Hz? 
</dt> <dd>

O Direct3D 9 tinha uma limitação no número de chamadas de desenho devido ao custo de CPU por chamada de desenho. No Direct3D 10, o custo de cada chamada de desenho foi reduzido. No entanto, não há mais uma correlação definitiva entre as chamadas de desenho e as taxas de quadros. Como as chamadas Draw geralmente exigem muitas chamadas de suporte (atualizações de buffer de constantes, associações de textura, configuração de estado e assim por diante), o impacto da taxa de quadros da API agora é mais dependente do uso geral da API em vez de simplesmente desenhar contagens de chamadas.

</dd> </dl>

## <a name="resources"></a>Recursos

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Que tipo de uso de recursos devo usar para as operações? 
</dt> <dd>

Use a seguinte folha de consulta:

-   A CPU atualiza o recurso mais de uma vez por quadro: D3D10 \_ uso \_ dinâmico
-   A CPU atualiza o recurso menos de uma vez por quadro: \_ padrão de uso d3d10 \_
-   A CPU não atualiza o recurso: D3D10 \_ uso \_ imutável
-   A CPU precisa ler o recurso: preparo de \_ uso de d3d10 \_

Como os buffers de constante sempre devem ser atualizados com frequência, eles não estão em conformidade com a "folha de dicas". Para os tipos de recursos a serem usados para buffers de constantes, consulte a seção [buffers de constantes](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>O que aconteceu com DrawPrimitiveUP e DrawIndexedPrimitiveUP? 
</dt> <dd>

Eles ficaram em D3D10. Para geometria dinâmica, use um \_ buffer dinâmico de uso d3d10 grande \_ . No início do quadro, mapeie-o com o D3D10 \_ map \_ Write \_ Discard. Para cada chamada de desenho subsequente, avance o ponteiro de gravação após a posição dos vértices desenhados anteriormente e mapeie o buffer com D3D10 \_ map \_ Write \_ sem \_ substituição. Se você estiver próximo do final do buffer antes do final do quadro, empacote o ponteiro de gravação em volta ao início e ao mapa com \_ descarte de gravação do mapa de d3d10 \_ \_ .

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Posso escrever índices de 16 bits e índices de 32 bits no mesmo buffer de geometria dinâmica? 
</dt> <dd>

Sim, você pode, mas isso pode incorrer em uma penalidade de desempenho em determinado hardware. É mais seguro criar buffers separados para dados de índice dinâmico de 16 bits e dados de índice de 32 bits.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Como fazer ler dados de volta da GPU para a CPU? 
</dt> <dd>

Você deve usar um recurso de preparo. Copie os dados do recurso de GPU para o recurso de preparo usando CopyResource. Mapeie o recurso de preparo para ler os dados.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Meu aplicativo era dependente da funcionalidade de StretchRect. 
</dt> <dd>

Como esse era essencialmente um wrapper para a funcionalidade básica do Direct3D, ele foi removido da API. Algumas das funcionalidades StretchRect foram movidas para D3DX10LoadTextureFromTexture. Para conversões de formato e cópia de texturas, D3DX10LoadTextureFromTexture pode fazer o trabalho. No entanto, as operações como a conversão de um tamanho para outra provavelmente exigirão um processamento para a operação de textura no aplicativo.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Não há deslocamentos ou tamanhos em chamadas de mapa para recursos. Eles estavam lá em chamadas de bloqueio no Direct3D 9; Por que eles mudaram? 
</dt> <dd>

Os deslocamentos e tamanhos nas chamadas de bloqueio no Direct3D 9 eram basicamente uma desordem na API e, muitas vezes, ignorados pelo driver. Os deslocamentos devem ser calculados em vez do aplicativo do ponteiro retornado na chamada de mapa.

</dd> </dl>

## <a name="depth-as-texture"></a>Profundidade como textura

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Que é mais rápido? Usar profundidade como uma textura ou uma profundidade de escrita em alfa e lendo isso? 
</dt> <dd>

Isso é específico de aplicativo e hardware. Use aquele que salvar a maior largura de banda. Se você já estiver usando vários destinos de renderização e tiver um canal extra, a criação de profundidade do sombreador pode ser uma solução melhor. Além disso, escrever profundidade para alfa ou outro destino de renderização permite que você escreva valores de profundidade linear que podem acelerar os cálculos que precisam acessar o buffer de profundidade.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Posso ter uma textura ligada como entrada e associada como uma textura de estêncil de profundidade, desde que eu desabilite gravações de profundidade? 
</dt> <dd>

Não está em D3D10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Posso resolver uma textura de estêncil de profundidade de MSAA? 
</dt> <dd>

Não está em D3D10. No entanto, você pode exemplificar exemplos individuais da textura MSAA. Consulte a seção [HLSL](#hlsl) para obter detalhes.

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Por que meu aplicativo falha assim que eu habilito o MSAA? 
</dt> <dd>

Verifique se você está habilitando uma contagem de exemplo de MSAA e um número de qualidade que, na verdade, são enumerados pelo driver.

</dd> </dl>

## <a name="crashes"></a>Falhas

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Meu aplicativo falha no D3D10 ou no driver e eu não sei por quê. 
</dt> <dd>

A primeira etapa é habilitar o tempo de execução de depuração ([**d3d10 criar sinalizador de \_ \_ \_ depuração de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) passado para [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Isso vai expor os erros mais comuns como saída de depuração.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>O PIX falha ao tentar usar meu aplicativo com ele. 
</dt> <dd>

A primeira etapa é habilitar o tempo de execução de depuração ([**d3d10 criar sinalizador de \_ \_ \_ depuração de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) passado para [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). O PIX tem uma probabilidade muito maior de falhar se a saída de depuração não estiver limpa.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Meu jogo fica sem espaço de endereço virtual no vista de 32 bits em D3D10. Ele não tem problemas no D3D9. 
</dt> <dd>

Houve alguns problemas com o D3D10 e o espaço de endereço virtual. Isso foi corrigido em [KB940105](https://support.microsoft.com/kb/940105). Se isso não corrigir o problema, verifique se você não está criando mais recursos que podem ser mapeados (bloqueados) em D3D10 do que você estava criando no D3D9. Além disso, pense em portar para 64 bits, já que isso se tornará mais predominante no futuro.

</dd> </dl>

## <a name="predicated-rendering"></a>Renderização de predicado

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Usei renderização predicado (com base nos resultados da consulta oclusão). Por que meu aplicativo ainda é a mesma velocidade? 
</dt> <dd>

Primeiro, verifique se a renderização que você gostaria de ignorar é, na verdade, o afunilamento do aplicativo. Se não for o afunilamento, ignorar a renderização não ajudará a taxa de quadros.

Em segundo lugar, certifique-se de que o tempo suficiente tenha passado entre o problema da consulta e a renderização que você deseja predicado. Se a consulta não tiver sido concluída no momento em que a chamada de renderização atingir a GPU, a renderização ocorrerá de qualquer forma.

Terceiro, predicação apenas ignora determinadas chamadas. As chamadas que são ignoradas são desenhar, limpar, copiar, atualizar, ResolveSubresource e GenerateMips. Configurações de estado, instalação de IA, mapear e criar chamadas não respeitam predicação. Se houver muitas chamadas de configuração de estado em relação à chamada de desenho a ser preparada, esses Estados ainda serão definidos.

</dd> </dl>

## <a name="geometry-shader"></a>Sombreador de geometria

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Devo usar o sombreador Geometry para incluí meu (inserir algo aqui)? 
</dt> <dd>

Não. O sombreador de geometria não deve ser usado para mosaico.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Posso usar o sombreador Geometry para criar geometria? 
</dt> <dd>

Sim, em cenários muito limitados. O sombreador de geometria nas partes D3D10 (2008) atuais não está equipado para lidar com muita expansão. Isso pode ser alterado no futuro. Os fornecedores de placas de vídeo podem ter um caminho especial para uma a quatro expansões devido a um hardware de ponto-Sprite existente. Qualquer outra expansão teria de ser muito limitada. Os exemplos de ParticlesGS e PipesGS atingem altas taxas de quadros apenas com a expansão limitada. Apenas alguns pontos são expandidos por quadro.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Para que devo usar o sombreador Geometry? 
</dt> <dd>

Qualquer coisa que exija operações em um primitivo inteiro, como detecção de silhueta, coordenadas barycentric e assim por diante. Use-o também para selecionar a qual fatia de uma matriz de destino de renderização enviar primitivos.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Posso gerar quantidades variáveis de geometria a partir do sombreador Geometry? 
</dt> <dd>

Sim, mas isso pode causar problemas de desempenho. Veja o exemplo de saída de 1 ponto para uma invocação e 4 pontos para outro. Ao se ajustar nas diretrizes de expansão, isso pode fazer com que os threads do sombreador de geometria sejam executados em série.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Como o D3D10 sabe como gerar índices de adjacência para minha malha? Ou, por que o D3D10 não é renderizado corretamente quando eu especificar que o sombreador Geometry precisa de informações de adjacência. 
</dt> <dd>

As informações de adjacência não são criadas por D3D10, mas pelo aplicativo. Os índices de adjacência são gerados pelo aplicativo e devem conter seis índices por primitivo; dos seis, os índices numerados ímpares são os vértices adjacentes da borda. ID3DX10Mesh:: GenerateAdjacencyAndPointsReps pode ser usado para gerar esses dados.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Há instruções de inteiro e bit-de-processo lentas? 
</dt> <dd>

Eles podem ser. Vários cartões D3D10 podem ser capazes de emitir operações de inteiros em um subconjunto das unidades de ALU disponíveis. Isso é altamente dependente do hardware. Consulte seu fornecedor de hardware individual para obter recomendações sobre como tratar operações de inteiros nesse hardware específico. Além disso, tenha muito cuidado com as conversões entre os tipos.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>O que aconteceu com o VPOS? 
</dt> <dd>

Se você declarar uma entrada para o sombreador de pixel como posição da VA \_ , obterá o mesmo comportamento que declará-la como VPOS.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Como fazer um exemplo de textura de MSAA? 
</dt> <dd>

No sombreador, declare sua textura como Texture2DMS. Em seguida, você pode buscar exemplos individuais usando os métodos de exemplo fora do objeto Texture2DMS.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Como fazer dizer se uma variável de sombreador em um buffer de constantes realmente é usada? 
</dt> <dd>

Examine a \_ estrutura desc de variável do sombreador d3d10 refletida \_ \_ para essa variável. uFlags deve ter o sinalizador de D3D10 \_ SVF \_ usado.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Como fazer dizer se uma variável de sombreador em um buffer constante realmente está usando FX10? 
</dt> <dd>

Atualmente, isso não é possível usando FX10.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Não tenho controle sobre os buffers de constantes que o FX10 cria. Como eles são criados e atualizados? 
</dt> <dd>

Todos os buffers de constante gerenciados por FX10 são criados como \_ recursos padrão de uso de d3d10 \_ e atualizados usando UpdateSubresource. Como o FX10 mantém um repositório de backup de todos os dados constantes, UpdateSubresource é a melhor abordagem para atualizá-los.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Como fazer emular o pipeline de função fixa usando sombreadores? 
</dt> <dd>

Consulte o exemplo de FixedFuncEMU.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Devo usar o novo \[ relance \] , \[ loop \] , \[ ramificação \] , e assim por diante, dicas de compilador? 
</dt> <dd>

Em geral, não. O compilador geralmente tentará as duas formas e escolherá a mais rápida. Em alguns casos, pode ser necessário usar \[ unroll \] , por exemplo, quando uma busca de textura dentro de um loop precisa de acesso a um gradiente.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>A precisão parcial faz alguma diferença no D3D10? Posso especificar a precisão parcial em meu D3D9 HLSL, mas não em meu D3D10 HLSL. 
</dt> <dd>

Todas as operações de D3D10 são especificadas para serem executadas com precisão de ponto flutuante de 32 bits. Portanto, a precisão parcial não deve fazer nenhuma diferença no D3D10.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>No D3D9, eu poderia fazer a filtragem de sombra do PCF de HW ligando um buffer de profundidade como uma textura e usando instruções regulares de HLSL de tex2d. Como fazer fazer isso no D3D10? 
</dt> <dd>

Você precisa usar um estado de amostra de comparação e usar instruções de SampleCmp.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Como essa palavra-chave Register funciona no D3D10? 
</dt> <dd>

A palavra-chave register em D3D10 agora se aplica a qual slot um recurso específico está associado. Nesse caso, o recurso pode ser um buffer (constante ou, caso contrário), textura ou amostra.

-   Para buffers de constantes, use a sintaxe: Register (bilhão), em que N é o slot de entrada (0-15)
-   Para texturas, use a sintaxe: Register (tN), em que N é o slot de entrada (0-127)
-   Para os exemplos, use a sintaxe: Register (sN), em que N é o slot de entrada (0-127)

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Como fazer Coloque uma variável dentro de um buffer de constantes se o registro for usado apenas para especificar onde associar o buffer inteiro? 
</dt> <dd>

Use a palavra-chave packoffset. O argumento para packoffset está na forma de c \[ 0-4095 \] . \[ x, y, z, w \] . Por exemplo:

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

Nesse buffer de constante, IWaste2Floats é colocado no terceiro float (12 bytes) no buffer de constantes. IWasteMore é colocado no 13 FLOAT4 ou 52nd float no buffer de constantes.

</dd> </dl>

 

 