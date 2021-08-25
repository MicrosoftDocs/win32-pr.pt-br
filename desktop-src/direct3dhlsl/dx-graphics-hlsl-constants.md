---
title: Constantes de sombreador (HLSL)
description: No Modelo de Sombreador 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- buffer constante
- buffer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a6b2ffa9168e870aeb405badb6ff71b0a4a59b23d76947e56a9c085ed0107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726546"
---
# <a name="shader-constants-hlsl"></a>Constantes de sombreador (HLSL)

No Modelo de Sombreador 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória. Eles podem ser organizados em dois tipos de buffers: buffers constantes (cbuffers) e buffers de textura (tbuffers). Buffers constantes são otimizados para uso de constante variável, o que é caracterizado pelo acesso de menor latência e atualização mais frequente da CPU. Por esse motivo, as restrições adicionais de tamanho, layout e acesso se aplicam a esses recursos. Os buffers de textura são acessados como texturas e têm um desempenho melhor para dados indexados arbitrariamente. Independentemente do tipo de recurso usado, não há limite para o número de buffers constantes ou buffers de textura que um aplicativo pode criar.

Declarar um buffer constante ou um buffer de textura se parece muito com uma declaração de estrutura em C, com a adição das palavras-chave **register** e **packoffset** para atribuir manualmente registros ou empacotar dados.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nome* \] \[: **register**(b \# ) { \] *VariableDeclaration:* \[ **packoffset**(c \# .xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[em \] O tipo de buffer.



| BufferType | Descrição     |
|------------|-----------------|
| cbuffer    | buffer constante |
| tbuffer    | buffer de textura  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

\[em \] Opcional, cadeia de caracteres ASCII que contém um nome de buffer exclusivo.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )
</dt> <dd>

\[em \] Palavra-chave opcional, usada para empacotar manualmente dados constantes. As constantes podem ser empacotadas em um registro somente em um buffer constante, em que o registro inicial é dado pelo número do registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[em \] Declaração de variável, semelhante a uma declaração de membro de estrutura. Pode ser qualquer tipo HLSL ou objeto de efeito (exceto uma textura ou um objeto de amostra).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)
</dt> <dd>

\[em \] Palavra-chave opcional, usada para empacotar manualmente dados constantes. As constantes podem ser empacotadas em qualquer buffer constante, em que o número do registro é dado por ( *\#* ). O empacotamento de subconjunto (usando o swizzling xyzw) está disponível para constantes cujo tamanho se ajusta a um único registro (não cruze um limite de registro). Por exemplo, um float4 não pôde ser empacotado em um único registro começando com o componente y porque ele não caberia em um registro de quatro componentes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.

Um buffer constante é um recurso de buffer especializado que é acessado como um buffer. Cada buffer constante pode conter até 4096 [vetores](dx-graphics-hlsl-vector.md); cada vetor contém até quatro valores de 32 bits. Você pode vincular até 14 buffers constantes por estágio de pipeline (dois slots adicionais são reservados para uso interno).

Um buffer de textura é um recurso de buffer especializado que é acessado como uma textura. O acesso à textura (em comparação com o acesso ao buffer) pode ter um melhor desempenho para dados indexados arbitrariamente. Você pode vincular até 128 buffers de textura por estágio de pipeline.

Um recurso de buffer foi projetado para minimizar a sobrecarga da configuração de constantes do sombreador. A estrutura de efeito (consulte [**Interface ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gerenciará a atualização de buffers de constante e textura, ou você pode usar a API do Direct3D para atualizar buffers (consulte Copiando e acessando dados de recursos [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obter informações. Um aplicativo também pode copiar dados de outro buffer (como um destino de renderização ou um destino de saída de fluxo) em um buffer constante.

Para obter mais informações sobre como usar buffers constantes em um aplicativo D3D10, consulte Tipos de recursos [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e Criando recursos de [buffer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Para obter mais informações sobre como usar buffers constantes em um aplicativo D3D11, consulte Introdução aos buffers no [Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [Como criar um buffer constante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

Um buffer constante não exige que uma [exibição](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) seja vinculada ao pipeline. No entanto, um buffer de textura requer uma exibição e deve ser vinculado a um slot de textura (ou deve ser vinculado com [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) ao usar um efeito).

Há duas maneiras de empacotar dados de constantes: usando as palavras-chave [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

Diferenças entre o Direct3D 9 e o Direct3D 10 e 11:

- Ao contrário da alocação automática de constantes no Direct3D 9, que não realizou o empacotamento e, em vez disso, atribuiu cada variável a um conjunto de registros float4, as variáveis de constante HLSL seguem regras de empacotamento no Direct3D 10 e 11.



 

### <a name="organizing-constant-buffers"></a>Organizar buffers constantes

Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.

O melhor modo de usar buffers constantes de modo eficiente é organizar as variáveis de sombreador em buffers constantes com base na frequência de atualização. Isso permite que um aplicativo minimize a largura de banda necessária para atualizar as constantes do sombreador. Por exemplo, um sombreador pode declarar dois buffers constantes e organizar os dados em cada um com base em sua frequência de atualização: os dados que precisam ser atualizados por objeto (como uma matriz mundial) são agrupados em um buffer constante que pode ser atualizado para cada objeto. Isso é separado dos dados que caracterizam uma cena e, portanto, provavelmente serão atualizados com muito menos frequência (quando a cena mudar).


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>Buffers constantes padrão

Há dois buffers constantes padrão disponíveis, $Global e $Param. As variáveis colocadas no escopo global são adicionadas implicitamente ao $Global cbuffer, usando o mesmo método de empacotamento usado para cbuffers. Parâmetros uniformes na lista de parâmetros de uma função aparecem no buffer $Param constante quando um sombreador é compilado fora da estrutura de efeitos. Quando compilados dentro da estrutura de efeitos, todos os uniformes devem resolver para as variáveis definidas no escopo global.

## <a name="examples"></a>Exemplos

Aqui está um exemplo de [Amostra Deslinhada10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que é um buffer de textura com uma matriz de matrizes.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Esta declaração de exemplo atribui manualmente um buffer constante para iniciar em um registro específico e também empacota elementos específicos por subcomponentes.


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

