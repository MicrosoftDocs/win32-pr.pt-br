---
title: Sombreadores de software
description: Os sombreadores de software são implementados para permitir o desenvolvimento de sombreadores sem suporte de hardware subjacente. Eles dão suporte ao conjunto de recursos completo. Como eles são implementados no software, eles não produzirão o melhor desempenho.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006190"
---
# <a name="software-shaders"></a>Sombreadores de software

Os sombreadores de software são implementados para permitir o desenvolvimento de sombreadores sem suporte de hardware subjacente. Eles dão suporte ao conjunto de recursos completo. Como eles são implementados no software, eles não produzirão o melhor desempenho.



| Versão   | Conjunto de recursos                  | Requisitos                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ SW | Todos os recursos do vs \_ 2 \_ x | Compatível apenas com o processamento de vértice de software e um dispositivo de referência. |
| vs \_ 3 \_ SW | Todos os recursos do vs \_ 3 \_ 0 | Compatível apenas com o processamento de vértice de software e um dispositivo de referência. |
| PS \_ 2 \_ SW | Todos os recursos do PS \_ 2 \_ x | Somente com suporte em um dispositivo de referência.                                |
| PS \_ 3 \_ SW | Todos os recursos do PS \_ 3 \_ 0 | Somente com suporte em um dispositivo de referência.                                |



 

Algumas validações são relaxadas para os sombreadores de software. Isso é útil para fins de depuração e protótipos. As validações a seguir são relaxadas: (todas as outras validações permanecem as mesmas)



| Tipo de validação                                 | Relaxamento                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contagens de instrução:                             | Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW. Instruções ilimitadas são permitidas.                                                                                                              |
| Contagens de constantes flutuantes:                          | Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW. São permitidas até 8192 constantes.                                                                                                                |
| Contagens de constantes inteiras:                        | Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW. São permitidas até 2048 constantes.                                                                                                                |
| Contagens de constantes boolianas:                        | Isso é relaxado para vs \_ 2 SW \_ , vs \_ 3 SW \_ e PS \_ 2 \_ SW, PS \_ 3 \_ SW. São permitidas até 2048 constantes.                                                                                                                |
| Dependente-ler profundidade:                           | Isso é relaxado para \_ o \_ software PS 2. Como no vs \_ 3 \_ 0 e no PS \_ 3 \_ 0, leituras dependentes ilimitadas são permitidas.                                                                                                                |
| Número de instruções e rótulos de controle de fluxo: | Isso é relaxado para o vs \_ 2 \_ SW. São permitidas instruções de controle de fluxo ilimitadas e até 2048 rótulos.                                                                                                                |
| Contagem de loops/início/etapa:                          | Eles são relaxados para o vs \_ 2 SW \_ , vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW. O tamanho da etapa de início e de interseção de iteração para instruções de rep e loop são intergers assinadas de 32 bits. A contagem de interativação pode ser até o máximo \_ int/64. |
| Limites de porta de leitura:                               | vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW não têm nenhum limite de porta de leitura.                                                                                                                                              |
| Número de interpoladores:                        | Há 16 [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) em vs \_ 3 \_ SW e 10 [PS \_ 3 \_ 0 registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) para o PS \_ 3 \_ SW.     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador ASM](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




