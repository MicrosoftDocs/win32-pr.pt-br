---
title: Sintaxe de Variável
description: Use as seguintes regras de sintaxe para declarar variáveis HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintaxe de variável (DirectX HLSL)
- nointerpolation, sintaxe de variável (DirectX HLSL)
- shared, Variable Syntax (DirectX HLSL)
- groupshared, sintaxe de variável (DirectX HLSL)
- static, Variable Syntax (DirectX HLSL)
- Sintaxe uniforme e variável (DirectX HLSL)
- volatile, Variable Syntax (DirectX HLSL)
- sintaxe precisa e variável (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ce89287d969683b72eb6db6d352300ce5295852
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481162"
---
# <a name="variable-syntax"></a>Sintaxe de Variável

Use as seguintes regras de sintaxe para declarar variáveis HLSL.

\[*Armazenamento \_ Índice* \] \[ *de nome do \_ tipo modificador* \] *de* \[ *tipo de* \] \[ *classe: semântico:* \] \[ *Packoffset:* \] \[ *Register* \] ;    \[  \] Anotações \[ *= Inicial \_ Valor*                    \]



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Armazenamento Classe* 
</dt> <dd>

Modificadores opcionais de classe de armazenamento que dão dicas do compilador sobre o escopo e o tempo de vida da variável; os modificadores podem ser especificados em qualquer ordem.




| Valor | Descrição | 
|-------|-------------|
| <strong>extern</strong> | Marcar uma variável global como uma entrada externa para o sombreador; essa é a marcação padrão para todas as variáveis globais. Não pode ser combinado com <strong>estático.</strong> | 
| <strong>nointerpolation</strong> | Não interpole as saídas de um sombreador de vértice antes de passá-las para um sombreador de pixel. | 
| <strong>Preciso</strong> | A <strong>palavra-chave</strong> precisa quando aplicada a uma variável restringirá todos os cálculos usados para produzir o valor atribuído a essa variável das seguintes maneiras:* Operações separadas são mantidas separadas. Por exemplo, em que uma operação mul e add pode ter sido mesclada em uma operação desarmada, <strong>a</strong> precisão força as operações a permanecerem separadas. Em vez disso, você deve usar explicitamente a função intrínseco.* A ordem das operações é mantida. Em que a ordem das instruções pode ter sido embaralhada para melhorar o <strong>desempenho,</strong> o compilador garante que a ordem preservada como escrita.* As operações não seguras do IEEE são restritas. Em que o compilador pode ter usado operações matemáticas rápidas que não são contabilizar valores de NaN (não um número) e INF (infinito), a precisão força os requisitos de IEEE relativos aos valores NaN e INF a serem respeitados. <strong></strong> Sem <strong>precisão</strong>, essas otimizações e operações matemáticas não <strong></strong> são seguras IEEE.* Qualificar uma variável precisa não faz operações que usam a variável <strong>precisa.</strong> Como <strong></strong> a precisão se propaga somente para operações que <strong></strong>contribuem para os valores <strong>atribuídos</strong> à variável qualificada de precisão, fazer cálculos desejados com precisão pode ser complicado, portanto, recomendamos marcar as saídas do sombreador diretamente onde você as declara, seja em um campo de estrutura ou em um parâmetro de saída ou o tipo de retorno da função de entrada. <strong></strong> A capacidade de controlar otimizações dessa maneira mantém a invariância de resultado para a variável de saída modificada desabilitando otimizações que podem afetar os resultados finais devido a diferenças nas diferenças de precisão acumuladas. É útil quando você deseja que sombreadores para mosaico mantenham as marcas de patch com água rígida ou que corresponderem aos valores de profundidade em várias passagens. [Código de exemplo:](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)```HLSLmatrix g_mWorldViewProjection;void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position){  // operation is precise because it contributes to the precise parameter OutPos  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );}``` | 
| <strong>Compartilhado</strong> | Marcar uma variável para compartilhamento entre efeitos; essa é uma dica para o compilador. | 
| <strong>groupshared</strong> | Marque uma variável para memória compartilhada de grupo de threads para sombreadores de computação. Em D3D10, o tamanho total máximo de todas as variáveis com a classe de armazenamento groupshared é de 16kb; em D3D11, o tamanho máximo é 32kb. Veja exemplos. | 
| <strong>static</strong> | Marque uma variável local para que ela seja inicializada uma vez e persista entre chamadas de função. Se a declaração não incluir um inicializador, o valor será definido como zero. Uma variável global marcada <strong>como estática</strong> não é visível para um aplicativo. | 
| <strong>uniforme</strong> | Marcar uma variável cujos dados são constantes durante a execução de um sombreador (como uma cor de material em um sombreador de vértice); as variáveis globais são <strong>consideradas uniformes</strong> por padrão. | 
| <strong>volatile</strong> | Marcar uma variável que muda com frequência; essa é uma dica para o compilador. Esse modificador de classe de armazenamento se aplica somente a uma variável local.<br /><blockquote>[!Note]<br />Atualmente, o compilador HLSL ignora esse modificador de classe de armazenamento.</blockquote><br /> | 




 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Modificador \_ de tipo*
</dt> <dd>

Modificador de tipo variável opcional.



| Valor             | Descrição                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Marque uma variável que não pode ser alterada por um sombreador, portanto, ela deve ser inicializada na declaração de variável. As variáveis globais são **consideradas const** por padrão (suprir esse comportamento fornecendo o sinalizador /Gec ao compilador). |
| **row \_ major**    | Marque uma variável que armazena quatro componentes em uma única linha para que eles possam ser armazenados em um único registro constante.                                                                                                                             |
| **coluna \_ principal** | Marque uma variável que armazena quatro componentes em uma única coluna para otimizar a matemática da matriz.                                                                                                                                                         |



 

> [!Note]  
> Se você não especificar um valor modificador de tipo, o compilador usará a **coluna \_ principal** como o valor padrão.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*
</dt> <dd>

Qualquer tipo HLSL listado em [Tipos de Dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ *Índice*\]
</dt> <dd>

Cadeia de caracteres ASCII que identifica exclusivamente uma variável de sombreador. Para definir uma matriz opcional, use **o índice para** o tamanho da matriz, que é um inteiro positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântica*
</dt> <dd>

Informações opcionais de uso de parâmetro, usadas pelo compilador para vincular entradas e saídas do sombreador. Há várias semânticas [predefinida](dx-graphics-hlsl-semantics.md) para sombreadores de vértice e pixel. O compilador ignora a semântica, a menos que elas sejam declaradas em uma variável global ou um parâmetro passado para um sombreador.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Palavra-chave opcional para empacotar manualmente as constantes do sombreador. Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registrar*
</dt> <dd>

Palavra-chave opcional para atribuir manualmente uma variável de sombreador a um registro específico. Consulte [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotações*
</dt> <dd>

Metadados opcionais, na forma de uma cadeia de caracteres, anexados a uma variável global. Uma anotação é usada pela estrutura de efeito e ignorada por HLSL; para ver uma sintaxe mais detalhada, consulte [sintaxe de anotação](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Valor \_ inicial*
</dt> <dd>

Valores iniciais opcionais; o número de valores deve corresponder ao número de componentes no *Tipo*. Cada variável global marcada **como extern** deve ser inicializada com um valor literal; cada variável **marcada como estática** deve ser inicializada com uma constante.

As variáveis globais que não estão **marcadas como** estáticas ou **extern** não são compiladas no sombreador. O compilador não configura automaticamente valores padrão para variáveis globais e não pode usá-los em otimizações. Para inicializar esse tipo de variável global, use reflexão para obter seu valor e, em seguida, copie o valor para um buffer constante. Por exemplo, você pode usar o método [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obter a variável, usar o método [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obter a descrição da variável de sombreador e obter o valor inicial do membro **DefaultValue** da estrutura [**D3D11 \_ SHADER \_ VARIABLE \_ DESC.**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) Para copiar o valor para o buffer constante, você deve garantir que o buffer foi criado com acesso de gravação da CPU ([**D3D11 \_ CPU \_ ACCESS \_ WRITE).**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag) Para obter mais informações sobre como criar um buffer constante, consulte [Como criar um buffer constante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)

Você também pode usar a estrutura [de efeitos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para processar automaticamente o refletindo e definindo o valor inicial. Por exemplo, você pode usar o [**método ID3DX11EffectPass::Apply.**](/windows/desktop/direct3d11/id3dx11effectpass-apply)

</dd> </dl>

## <a name="examples"></a>Exemplos

Aqui estão vários exemplos de declarações de variável de sombreador.


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>Grupo Compartilhado

O HLSL permite que threads de um sombreador de computação troquem valores por meio de memória compartilhada. O HLSL fornece primitivos de barreira, como [**GroupMemoryBaoryWithGroupSync**](groupmemorybarrierwithgroupsync.md)e assim por diante, para garantir a ordenação correta de leituras e gravações na memória compartilhada no sombreador e evitar a corrida de dados.

> [!Note]  
> O hardware executa threads em grupos (distorções ou frontes de onda) e a sincronização de barreira às vezes pode ser omitida para aumentar o desempenho quando apenas os threads de sincronização que pertencem ao mesmo grupo estão corretos. Mas é altamente recomendável essa omissão por estes motivos:
>
> -   Essa omissão resulta em código não portátil, que pode não funcionar em algum hardware e não funciona em rasterizadores de software que normalmente executam threads em grupos menores.
> -   As melhorias de desempenho que você pode obter com essa omissão serão secundárias em comparação com o uso da barreira de todos os threads.

 

No Direct3D 10, não há nenhuma sincronização de threads ao escrever em grupos **compartilhadas,** portanto, isso significa que cada thread está limitado a um único local em uma matriz para escrita. Use o [valor do sistema SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) para indexar nessa matriz ao escrever para garantir que nenhum dois threads possam colidir. Em termos de leitura, todos os threads têm acesso a toda a matriz para leitura.


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>Recibo

Pacotes subcomponentes de vetores e escalares cujo tamanho é grande o suficiente para evitar o cruzamento dos limites de registro. Por exemplo, todos eles são válidos:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Não é possível misturar tipos de empacotamento.

Assim como a palavra-chave Register, um packoffset pode ser específico de destino. A embalagem do subcomponente só está disponível com a palavra-chave packoffset, não a palavra-chave Register. Dentro de uma declaração CBuffer, a palavra-chave Register é ignorada para destinos do Direct3D 10, pois ela é considerada para compatibilidade entre plataformas.

Elementos empacotados podem se sobrepor e o compilador não apresentará nenhum erro ou aviso. Neste exemplo, Element2 e Element3 serão sobrepostas com Element1. x e Element1. y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Um exemplo que usa packoffset é: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Variáveis (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

