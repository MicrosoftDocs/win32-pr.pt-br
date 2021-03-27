---
title: Regras de empacotamento para variáveis constantes
description: As regras de empacotamento determinam como os dados rígidos podem ser organizados quando são armazenados.
ms.assetid: 5c399342-06e1-47d2-8ecf-e093ed04be50
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d85566083dc9ead93a1a9e73fb06051b62178114
ms.sourcegitcommit: 004d7881dc9ff92ea394cd2331774e13b1e7f13c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/12/2020
ms.locfileid: "103640366"
---
# <a name="packing-rules-for-constant-variables"></a>Regras de empacotamento para variáveis constantes

As regras de empacotamento determinam como os dados rígidos podem ser organizados quando são armazenados. O HLSL implementa regras de empacotamento para dados de saída do VS, dados de entrada e saída GS e dados de entrada e saída do PS. (Os dados não são empacotados para entradas do VS porque o estágio IA não pode desempacotar dados.)

As regras de empacotamento HLSL são semelhantes à execução de um **\# pragma Pack 4** com o Visual Studio, que empacota dados em limites de 4 bytes. Além disso, HLSL pacotes de dados para que ele não cruze um limite de 16 bytes. As variáveis são empacotadas em um determinado vetor de quatro componentes até que a variável se aprofunde em um limite de 4 vetores; as variáveis seguintes serão resaltadas para o próximo vetor de quatro componentes.

Cada estrutura força a próxima variável a iniciar no próximo vetor de quatro componentes. Às vezes, isso gera preenchimento para matrizes de estruturas. O tamanho resultante de qualquer estrutura será sempre divisível por **sizeof**(*vetor de quatro componentes*).

As matrizes não são empacotadas em HLSL por padrão. Para evitar forçar o sombreador a assumir a sobrecarga de ALU para cálculos de deslocamento, cada elemento em uma matriz é armazenado em um vetor de quatro componentes. Observe que você pode obter a embalagem para matrizes (e incorrer nos cálculos de endereçamento) usando a conversão.

Veja a seguir exemplos de estruturas e seus tamanhos de pacotes correspondentes (dado: um **float1** ocupa 4 bytes):


```
//  2 x 16byte elements
cbuffer IE
{
    float4 Val1;
    float2 Val2;  // starts a new vector
    float2 Val3;
};

//  3 x 16byte elements
cbuffer IE
{
    float2 Val1;
    float4 Val2;  // starts a new vector
    float2 Val3;  // starts a new vector
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val2;
    float2 Val3;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float2 Val2;
    float1 Val3;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float1 Val1;
    float2 Val2;    // starts a new vector
};


//  1 x 16byte elements
cbuffer IE
{
    float3 Val1;
    float1 Val2;
};

//  1 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float3 Val2;
};

//  2 x 16byte elements
cbuffer IE
{
    float1 Val1;
    float1 Val1;
    float3 Val2;        // starts a new vector
};


// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;

    struct     {
        float4 SVal1;    // starts a new vector
        float1 SVal2;    // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    float1 Val1;  
    struct     {
        float1 SVal1;     // starts a new vector
        float4 SVal2;     // starts a new vector
    } Val2;
};

// 3 x 16byte elements
cbuffer IE
{
    struct     {
        float4 SVal1;
        float1 SVal2;    // starts a new vector
    } Val1;

    float1 Val2; 
};
```



## <a name="more-aggressive-packing"></a>Empacotamento mais agressivo

Você pode empacotar uma matriz de forma mais agressiva. Por exemplo, dada uma matriz de variáveis float:


```
float4 array[16];
```



Você pode optar por fazer a compactação dessa forma, sem espaços na matriz:


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



A embalagem mais rígida é uma compensação em comparação com a necessidade de instruções adicionais do sombreador para o cálculo do endereço.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




