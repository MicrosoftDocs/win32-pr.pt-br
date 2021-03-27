---
title: Constantes de sombreador (HLSL)
description: No sombreador modelo 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffers
- buffer de constantes
- buffer de textura
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644132"
---
# <a name="shader-constants-hlsl"></a>Constantes de sombreador (HLSL)

No sombreador modelo 4, as constantes de sombreador são armazenadas em um ou mais recursos de buffer na memória. Eles podem ser organizados em dois tipos de buffers: buffers de constantes (cbuffers) e buffers de textura (tbuffers). Buffers de constantes são otimizados para uso de variável constante, que é caracterizado por acesso de menor latência e atualização mais frequente da CPU. Por esse motivo, o tamanho adicional, o layout e as restrições de acesso se aplicam a esses recursos. Os buffers de textura são acessados como texturas e têm melhor desempenho para dados indexados arbitrariamente. Independentemente do tipo de recurso usado, não há nenhum limite para o número de buffers de constantes ou buffers de textura que um aplicativo pode criar.

A declaração de um buffer de constantes ou de um buffer de textura parece muito parecida com uma declaração de estrutura em C, com a adição das palavras-chave **Register** e **packoffset** para atribuir manualmente registros ou dados de empacotamento.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nome* \] do \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[no \] tipo de buffer.



| BufferType | Description     |
|------------|-----------------|
| cbuffer    | buffer de constantes |
| tbuffers    | buffer de textura  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*
</dt> <dd>

\[em \] opcional, a cadeia de caracteres ASCII contendo um nome de buffer exclusivo.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**registrar**(b \# )
</dt> <dd>

\[na \] palavra-chave opcional, usada para empacotar manualmente os dados constantes. As constantes podem ser empacotadas em um registro somente em um buffer de constantes, em que o registro inicial é fornecido pelo número de registro ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[em \] declaração de variável, semelhante a uma declaração de membro de estrutura. Pode ser qualquer tipo de HLSL ou objeto de efeito (exceto um objeto de textura ou de amostra).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)
</dt> <dd>

\[na \] palavra-chave opcional, usada para empacotar manualmente os dados constantes. As constantes podem ser empacotadas em qualquer buffer constante, onde o número de registro é fornecido pelo ( *\#* ). A embalagem de subcomponente (usando xyzw swizzling) está disponível para constantes cujo tamanho se ajusta em um único registro (não cruzar um limite de registro). Por exemplo, um FLOAT4 não pôde ser empacotado em um único registro, começando com o componente y, porque ele não caberia em um registro de quatro componentes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.

Um buffer de constantes é um recurso de buffer especializado que é acessado como um buffer. Cada buffer de constantes pode conter até 4096 [vetores](dx-graphics-hlsl-vector.md); cada vetor contém até valores de 4 32 bits. Você pode associar até 14 buffers de constante por estágio de pipeline (2 slots adicionais são reservados para uso interno).

Um buffer de textura é um recurso de buffer especializado que é acessado como uma textura. O acesso à textura (em comparação com o acesso ao buffer) pode ter um desempenho melhor para dados indexados arbitrariamente. Você pode associar até 128 buffers de textura por estágio de pipeline.

Um recurso de buffer foi projetado para minimizar a sobrecarga de definir constantes de sombreador. A estrutura de efeito (consulte a [**interface ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gerenciará os buffers de textura e constante de atualização, ou você poderá usar a API do Direct3D para atualizar os buffers (consulte [copiando e acessando dados de recurso (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) para obter informações). Um aplicativo também pode copiar dados de outro buffer (como um destino de renderização ou um destino de saída de fluxo) em um buffer de constantes.

Para obter mais informações sobre como usar buffers de constantes em um aplicativo D3D10, consulte [tipos de recursos (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e [criando recursos de buffer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Para obter informações de Morel sobre como usar buffers de constantes em um aplicativo D3D11, consulte [introdução aos buffers no Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [como criar um buffer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Um buffer de constantes não requer uma [exibição](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) para ser associado ao pipeline. Um buffer de textura, no entanto, requer uma exibição e deve estar associado a um slot de textura (ou deve ser associado a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) ao usar um efeito).

Há duas maneiras de empacotar dados constantes: usando as palavras-chave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10 e 11:<br/> Ao contrário da alocação automática de constantes no Direct3D 9, que não executou a embalagem e, em vez disso, atribuiu cada variável a um conjunto de registros FLOAT4, as variáveis constantes HLSL seguem regras de empacotamento no Direct3D 10 e 11.<br/> |



 

### <a name="organizing-constant-buffers"></a>Organizando buffers de constantes

Buffers constantes reduzem a largura de banda necessária para atualizar constantes de sombreador, permitindo que as constantes de sombreador sejam agrupadas e confirmadas ao mesmo tempo em vez de fazer chamadas individuais para confirmar cada constante separadamente.

O melhor modo de usar buffers constantes de modo eficiente é organizar as variáveis de sombreador em buffers constantes com base na frequência de atualização. Isso permite que um aplicativo Minimize a largura de banda necessária para atualizar constantes de sombreador. Por exemplo, um sombreador pode declarar dois buffers constantes e organizar os dados em cada um com base em sua frequência de atualização: os dados que precisam ser atualizados por objeto (como uma matriz mundial) são agrupados em um buffer constante que pode ser atualizado para cada objeto. Isso é separado dos dados que caracterizam uma cena e, portanto, provavelmente serão atualizados com muito menos frequência (quando a cena for alterada).


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



### <a name="default-constant-buffers"></a>Buffers de constantes padrão

Há dois buffers de constante padrão disponíveis, $Global e $Param. Variáveis que são colocadas no escopo global são adicionadas implicitamente ao $Global CBuffer, usando o mesmo método de empacotamento usado para cbuffers. Os parâmetros uniformes na lista de parâmetros de uma função aparecem no buffer de constantes $Param quando um sombreador é compilado fora da estrutura de efeitos. Quando compilado dentro da estrutura de efeitos, todos os uniforms devem ser resolvidos para as variáveis definidas no escopo global.

## <a name="examples"></a>Exemplos

Aqui está um exemplo de exemplo de [Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) que é um buffer de textura composto por uma matriz de matrizes.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Essa declaração de exemplo atribui manualmente um buffer de constantes para iniciar em um registro específico e também empacota elementos específicos por subcomponentes.


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

 

