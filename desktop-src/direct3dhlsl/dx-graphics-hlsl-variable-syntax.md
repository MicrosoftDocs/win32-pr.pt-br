---
title: Sintaxe de Variável
description: Use as regras de sintaxe a seguir para declarar variáveis HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- externo, sintaxe de variável (DirectX HLSL)
- nointerpolação, sintaxe de variável (DirectX HLSL)
- Sintaxe compartilhada, variável (DirectX HLSL)
- groupshared, sintaxe de variável (DirectX HLSL)
- Sintaxe estática, variável (DirectX HLSL)
- Sintaxe uniforme e variável (DirectX HLSL)
- volátil, sintaxe de variável (DirectX HLSL)
- Sintaxe precisa, variável (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/11/2020
ms.locfileid: "104988724"
---
# <a name="variable-syntax"></a>Sintaxe de Variável

Use as regras de sintaxe a seguir para declarar variáveis HLSL.



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Armazenamento \_ do Tipo de classe* \] \[ *\_ modificador* \] *nome* \[ *índice* \] \[ *: semântica* \] \[ *: Packoffset* \] \[ *: registrar* \] ;    \[  \] Anotações \[ *= Inicial \_ Valor* do                    \] |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe de armazenamento \_* 
</dt> <dd>

Modificadores de classe de armazenamento opcionais que fornecem dicas de compilador sobre escopo de variável e tempo de vida; os modificadores podem ser especificados em qualquer ordem.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>extern</strong></td>
<td>Marcar uma variável global como uma entrada externa para o sombreador; Essa é a marcação padrão para todas as variáveis globais. Não pode ser combinado com <strong>static</strong>.</td>
</tr>
<tr class="even">
<td><strong>nointerpolação</strong></td>
<td>Não interpolar as saídas de um sombreador de vértice antes de passá-las para um sombreador de pixel.</td>
</tr>
<tr class="odd">
<td><strong>Precisas</strong></td>
<td>A palavra-chave <strong>precisa</strong> quando aplicada a uma variável restringirá quaisquer cálculos usados para produzir o valor atribuído a essa variável das seguintes maneiras:

*   Operações separadas são mantidas separadas. Por exemplo, onde um Mul e uma operação de adição podem ter sido fundidos em uma operação Mad, a <strong>precisão</strong> força as operações a permanecerem separadas. Em vez disso, você deve usar explicitamente a função intrínseca Mad.
*   A ordem das operações é mantida. Onde a ordem das instruções pode ter sido embaralhada para melhorar o desempenho, a <strong>precisão</strong> garante que o compilador preserve o pedido como escrito.
*   As operações IEEE não seguras são restritas. Onde o compilador pode ter usado operações matemáticas rápidas que não contenham valores NaN (não um número) e INF (infinitos), <strong>preciso</strong> força os requisitos de IEEE relacionados a valores Nan e inf a serem respeitados. Sem <strong>precisa</strong>, essas otimizações e operações matemáticas não são seguras para IEEE.
*   A qualificação de uma variável <strong>precisa</strong> não faz com que as operações usem a variável <strong>precisa</strong>. Como a propagação <strong>precisa</strong> apenas para as operações que contribuem com os valores atribuídos à variável qualificada com <strong>precisão</strong>, fazer <strong>os cálculos</strong> desejados corretamente pode ser complicado, portanto, recomendamos que você marque as saídas de sombreador de forma <strong>precisa</strong> diretamente onde declará-las, sejam elas em um campo de estrutura, ou em um parâmetro de saída, ou o tipo de retorno da função de entrada.

A capacidade de controlar otimizações dessa maneira mantém a invariação de resultado da variável de saída modificada desabilitando otimizações que podem afetar os resultados finais devido a diferenças nas diferenças de precisão acumuladas. É útil quando você deseja que os sombreadores para mosaico mantenham emendas de patches de água rígida ou valores de profundidade de correspondência em várias passagens.

[Código de exemplo](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl): 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><strong>compartilhado</strong></td>
<td>Marcar uma variável para compartilhamento entre os efeitos; Esta é uma dica para o compilador.</td>
</tr>
<tr class="odd">
<td><strong>groupshared</strong></td>
<td>Marque uma variável para a memória compartilhada do grupo de threads para sombreadores de computação. Em D3D10, o tamanho total máximo de todas as variáveis com a classe de armazenamento groupshared é 16 KB, em D3D11 o tamanho máximo é 32 KB. Consulte exemplos.</td>
</tr>
<tr class="even">
<td><strong>static</strong></td>
<td>Marque uma variável local para que ela seja inicializada uma vez e persiste entre as chamadas de função. Se a declaração não incluir um inicializador, o valor será definido como zero. Uma variável global marcada como <strong>estática</strong> não é visível para um aplicativo.</td>
</tr>
<tr class="odd">
<td><strong>universal</strong></td>
<td>Marcar uma variável cujos dados são constantes durante a execução de um sombreador (como uma cor de material em um sombreador de vértice); as variáveis globais são consideradas <strong>uniformes</strong> por padrão.</td>
</tr>
<tr class="even">
<td><strong>volatile</strong></td>
<td>Marcar uma variável que é alterada com frequência; Esta é uma dica para o compilador. Este modificador de classe de armazenamento só se aplica a uma variável local.<br/>
<blockquote>
[!Note]<br />
O compilador HLSL atualmente ignora esse modificador de classe de armazenamento.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificador de tipo*
</dt> <dd>

Modificador de tipo variável opcional.



| Valor             | Descrição                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Marque uma variável que não pode ser alterada por um sombreador, portanto, ela deve ser inicializada na declaração da variável. Variáveis globais são consideradas **const** por padrão (suprimir esse comportamento fornecendo o sinalizador/GEC para o compilador). |
| **linha \_ principal**    | Marque uma variável que armazena quatro componentes em uma única linha para que eles possam ser armazenados em um único registro constante.                                                                                                                             |
| **coluna \_ principal** | Marque uma variável que armazena 4 componentes em uma única coluna para otimizar a matriz matemática.                                                                                                                                                         |



 

> [!Note]  
> Se você não especificar um valor de modificador de tipo, o compilador usará a **coluna \_ principal** como o valor padrão.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Escreva*
</dt> <dd>

Qualquer tipo de HLSL listado em [tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ do *Índice* do\]
</dt> <dd>

Cadeia de caracteres ASCII que identifica exclusivamente uma variável de sombreador. Para definir uma matriz opcional, use **index** para o tamanho da matriz, que é um inteiro positivo = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântico*
</dt> <dd>

Parâmetro opcional-informações de uso, usadas pelo compilador para vincular entradas e saídas do sombreador. Há várias [semânticas](dx-graphics-hlsl-semantics.md) predefinidas para os sombreadores de vértices e de pixel. O compilador ignora a semântica, a menos que elas sejam declaradas em uma variável global ou um parâmetro passado para um sombreador.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Palavra-chave opcional para empacotar manualmente as constantes do sombreador. Consulte [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registr*
</dt> <dd>

Palavra-chave opcional para atribuir manualmente uma variável de sombreador a um registro específico. Consulte [registrar (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Anotação (ões)*
</dt> <dd>

Metadados opcionais, na forma de uma cadeia de caracteres, anexados a uma variável global. Uma anotação é usada pela estrutura de efeito e ignorada por HLSL; para ver a sintaxe mais detalhada, consulte a [sintaxe da anotação](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valor inicial*
</dt> <dd>

Valor (es) inicial (is) opcional (is); o número de valores deve corresponder ao número de componentes no *tipo*. Cada variável global marcada como **externa** deve ser inicializada com um valor literal; cada variável marcada como **static** deve ser inicializada com uma constante.

Variáveis globais que não são marcadas como **static** ou **extern** não são compiladas no sombreador. O compilador não define automaticamente valores padrão para variáveis globais e não pode usá-los em otimizações. Para inicializar esse tipo de variável global, use reflexão para obter seu valor e, em seguida, copie o valor para um buffer de constantes. Por exemplo, você pode usar o método [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) para obter a variável, usar o método [**ID3D11ShaderReflectionVariable:: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) para obter a descrição da variável de sombreador e obter o valor inicial do membro **DefaultValue** da estrutura [**\_ \_ \_ desc da variável do sombreador D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) . Para copiar o valor para o buffer de constantes, você deve garantir que o buffer foi criado com acesso de gravação de CPU ([**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)). Para obter mais informações sobre como criar um buffer de constantes, consulte [como criar um buffer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Você também pode usar a [estrutura de efeitos](../direct3d11/d3d11-graphics-programming-guide-effects.md) para processar automaticamente a reflexão e a definição do valor inicial. Por exemplo, você pode usar o método [**ID3DX11EffectPass:: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .

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



### <a name="group-shared"></a>Grupo compartilhado

O HLSL permite que threads de um sombreador de computação troquem valores por meio de memória compartilhada. O HLSL fornece primitivos de barreira como [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)e assim por diante para garantir a ordenação correta de leituras e gravações na memória compartilhada no sombreador e evitar corridas de dados.

> [!Note]  
> O hardware executa threads em grupos (warpes ou ondulados) e a sincronização de barreira, às vezes, pode ser omitida para aumentar o desempenho quando apenas os threads que pertencem ao mesmo grupo estão corretos. Mas não é altamente recomendável essa omissão por esses motivos:
>
> -   Essa omissão resulta em código não portátil, que pode não funcionar em algum hardware e não funciona em rasterizadores de software que normalmente executam threads em grupos menores.
> -   As melhorias de desempenho que você pode atingir com essa omissão serão pequenas em comparação com a barreira de todos os threads.

 

No Direct3D 10 não há sincronização de threads ao gravar em **groupshared**, portanto, isso significa que cada thread é limitado a um único local em uma matriz para gravação. Use o valor do sistema [ \_ GroupIndex VA](dx-graphics-hlsl-semantics.md) para indexar nessa matriz ao gravar para garantir que dois threads possam colidir. Em termos de leitura, todos os threads têm acesso a toda a matriz para leitura.


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

 

