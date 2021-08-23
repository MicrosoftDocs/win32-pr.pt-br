---
description: O Direct3D 9 dá suporte a pontos, linhas, triângulos e primitivos de grade.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Primitivos de Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36ee67cfe4d4a802303091288f3906778e6cb3cdc1ad811602a80bc161d0a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122117"
---
# <a name="higher-order-primitives-direct3d-9"></a>Primitivos de Higher-Order (Direct3D 9)

O Direct3D 9 dá suporte a pontos, linhas, triângulos e primitivos de grade. Elas foram estendidas para dar suporte à interpolação de ordem mais alta além da linear. Enquanto os triângulos e as linhas têm a extensão espacial, até agora elas foram processadas usando interpolação linear. No Direct3D 9, o Direct3D dá suporte à renderização desses tipos primitivos usando ordem superior, até QUINTIC, interpolação. Além disso, agora há suporte para um novo tipo primitivo quádruplo. Esse novo tipo também pode ser renderizado com interpolação de ordem mais alta. Esse recurso é orientado principalmente pelos requisitos de animação e renderização de caracteres. Ele também pode ser usado para outras superfícies, como terreno ou água.

Os primitivos de ordem superior dão suporte à interpolação de ordem superior quando transmitidos para a API como listas, faixas, ventiladores ou malhas indexadas. Isso é obtido com o uso de informações adicionais codificadas nos próprios vértices. Por exemplo, vetores normais podem ser usados para definir os planos tangentes nos vértices para habilitar a interpolação cúbica. A maioria das implementações dá suporte à interpolação de ordem superior por mosaico em triângulos planar. A etapa de mosaico é aplicada logicamente antes do estágio de sombreador de vértice. Como a API do sombreador de vértice não impõe semânticas em seus dados de entrada, um mecanismo especial é fornecido para identificar o componente de fluxo de vértice que representa a posição e, opcionalmente, o vetor normal. Todos os outros componentes são interpolados de acordo.

Esta seção apresenta primitivos de ordem mais alta e discute como eles podem ser usados em seus aplicativos. As informações são divididas nos tópicos a seguir.

-   [Qualidade aprimorada por meio do aprimoramento de resolução](#improved-quality-through-resolution-enhancement)
-   [Mapeamento direto de ferramentas de Spline-Based](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Qualidade aprimorada por meio do aprimoramento de resolução

Os primitivos atuais não são ideais para representar superfícies suaves. Métodos de interpolação de ordem superior, como polinomiais cúbicos, permitem cálculos mais precisos na renderização de formas curvas. Isso proporciona um aumento de realm reduzindo ou eliminando artefatos de faceta visíveis em bordas de silhueta ou na iluminação de superfície especular. Além disso, quando o mosaico ocorre no chip, os triângulos mosaico não afetam a largura de banda do barramento. Em muitos casos, uma pequena quantidade de mosaicos pode fornecer melhorias na qualidade da imagem com impacto mínimo no desempenho.

O Direct3D 9 fornece uma maneira simples de aplicar o aprimoramento de resolução ao conteúdo criado por ferramentas orientadas a polígono existentes e pipelines de arte. A necessidade do aplicativo fornece apenas um nível desejado de mosaico e transmite os dados usando a sintaxe de triângulo padrão que inclui vetores normais.

## <a name="direct-mapping-from-spline-based-tools"></a>Mapeamento direto de ferramentas de Spline-Based

Muitas ferramentas de criação atuais dão suporte a primitivos de ordem mais alta para permitir operações de modelagem mais poderosas do que normalmente são fornecidas com malhas de triângulo planares. Quando usado com eficiência, para que o número de patches gerados seja razoável, essas ferramentas podem produzir conteúdo que pode ser renderizado diretamente pela API. Para atender a esse requisito, foi adicionado um novo ponto de entrada que interpreta o fluxo de dados de vértice de entrada como uma matriz 2D de pontos de controle e tessellates-lo à resolução desejada.

-   [Usando primitivos de Higher-Order (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 



