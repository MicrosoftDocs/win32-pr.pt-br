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
# <a name="packing-rules-for-constant-variables"></a><span data-ttu-id="4c0ea-103">Regras de empacotamento para variáveis constantes</span><span class="sxs-lookup"><span data-stu-id="4c0ea-103">Packing Rules for Constant Variables</span></span>

<span data-ttu-id="4c0ea-104">As regras de empacotamento determinam como os dados rígidos podem ser organizados quando são armazenados.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-104">Packing rules dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="4c0ea-105">O HLSL implementa regras de empacotamento para dados de saída do VS, dados de entrada e saída GS e dados de entrada e saída do PS.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-105">HLSL implements packing rules for VS output data, GS input and output data, and PS input and output data.</span></span> <span data-ttu-id="4c0ea-106">(Os dados não são empacotados para entradas do VS porque o estágio IA não pode desempacotar dados.)</span><span class="sxs-lookup"><span data-stu-id="4c0ea-106">(Data is not packed for VS inputs because the IA stage cannot unpack data.)</span></span>

<span data-ttu-id="4c0ea-107">As regras de empacotamento HLSL são semelhantes à execução de um **\# pragma Pack 4** com o Visual Studio, que empacota dados em limites de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-107">HLSL packing rules are similar to performing a **\#pragma pack 4** with Visual Studio, which packs data into 4-byte boundaries.</span></span> <span data-ttu-id="4c0ea-108">Além disso, HLSL pacotes de dados para que ele não cruze um limite de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-108">Additionally, HLSL packs data so that it does not cross a 16-byte boundary.</span></span> <span data-ttu-id="4c0ea-109">As variáveis são empacotadas em um determinado vetor de quatro componentes até que a variável se aprofunde em um limite de 4 vetores; as variáveis seguintes serão resaltadas para o próximo vetor de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-109">Variables are packed into a given four-component vector until the variable will straddle a 4-vector boundary; the next variables will be bounced to the next four-component vector.</span></span>

<span data-ttu-id="4c0ea-110">Cada estrutura força a próxima variável a iniciar no próximo vetor de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-110">Each structure forces the next variable to start on the next four-component vector.</span></span> <span data-ttu-id="4c0ea-111">Às vezes, isso gera preenchimento para matrizes de estruturas.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-111">This sometimes generates padding for arrays of structures.</span></span> <span data-ttu-id="4c0ea-112">O tamanho resultante de qualquer estrutura será sempre divisível por **sizeof**(*vetor de quatro componentes*).</span><span class="sxs-lookup"><span data-stu-id="4c0ea-112">The resulting size of any structure will always be evenly divisible by **sizeof**(*four-component vector*).</span></span>

<span data-ttu-id="4c0ea-113">As matrizes não são empacotadas em HLSL por padrão.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-113">Arrays are not packed in HLSL by default.</span></span> <span data-ttu-id="4c0ea-114">Para evitar forçar o sombreador a assumir a sobrecarga de ALU para cálculos de deslocamento, cada elemento em uma matriz é armazenado em um vetor de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-114">To avoid forcing the shader to take on ALU overhead for offset computations, every element in an array is stored in a four-component vector.</span></span> <span data-ttu-id="4c0ea-115">Observe que você pode obter a embalagem para matrizes (e incorrer nos cálculos de endereçamento) usando a conversão.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-115">Note that you can achieve packing for arrays (and incur the addressing calculations) by using casting.</span></span>

<span data-ttu-id="4c0ea-116">Veja a seguir exemplos de estruturas e seus tamanhos de pacotes correspondentes (dado: um **float1** ocupa 4 bytes):</span><span class="sxs-lookup"><span data-stu-id="4c0ea-116">Following are examples of structures and their corresponding packed sizes (given: a **float1** occupies 4 bytes):</span></span>


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



## <a name="more-aggressive-packing"></a><span data-ttu-id="4c0ea-117">Empacotamento mais agressivo</span><span class="sxs-lookup"><span data-stu-id="4c0ea-117">More Aggressive Packing</span></span>

<span data-ttu-id="4c0ea-118">Você pode empacotar uma matriz de forma mais agressiva.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-118">You could pack an array more aggressively.</span></span> <span data-ttu-id="4c0ea-119">Por exemplo, dada uma matriz de variáveis float:</span><span class="sxs-lookup"><span data-stu-id="4c0ea-119">For instance, given an array of float variables:</span></span>


```
float4 array[16];
```



<span data-ttu-id="4c0ea-120">Você pode optar por fazer a compactação dessa forma, sem espaços na matriz:</span><span class="sxs-lookup"><span data-stu-id="4c0ea-120">You could choose to pack it like this, without any spaces in the array:</span></span>


```
static float2 aggressivePackArray[32] = (float2[32])array;  
```



<span data-ttu-id="4c0ea-121">A embalagem mais rígida é uma compensação em comparação com a necessidade de instruções adicionais do sombreador para o cálculo do endereço.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-121">The tighter packing is a trade off versus the need for additional shader instructions for address computation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c0ea-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c0ea-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c0ea-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="4c0ea-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




