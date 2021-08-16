---
description: As diretivas do compilador ajustam a funcionalidade que a biblioteca DirectXMath usa.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Diretivas do compilador da Biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261b4d7dec2c9c3fda7413c0559ad95b7b6a46d31ad2f273c04c8e2bd4c30054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118206"
---
# <a name="directxmath-library-compiler-directives"></a>Diretivas do compilador da Biblioteca DirectXMath

As diretivas do compilador ajustam a funcionalidade que a biblioteca DirectXMath usa.



| Diretiva                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ SEM \_ INTRÍNSECOS\_        | Quando \_ XM \_ NO INTRINSICS é definido, as operações do \_ \_ DirectXMath são implementadas sem usar nenhum intrínseco específico da plataforma. Em vez disso, o DirectXMath usa apenas operações de ponto flutuante padrão.<br/> Por padrão, \_ XM \_ NO \_ INTRINSICS \_ não está definido.<br/> Essa diretiva substitui todas as outras diretivas. Portanto, recomendamos que você verifique XM NO INTRINSICS antes de determinar o status de INTRÍNSECOS DO XM ARM NEON ou \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTRÍNSECOS \_ de SSE \_ \_ XM.<br/>                                                                              |
| \_INTRÍNSECOS \_ DE SSE \_ XM\_       | Quando XM SSE INTRINSICS é definido, o código é compilado para usar SSE e \_ SSE2 de suporte em plataformas que suportam \_ \_ esses conjuntos de \_ instruções.<br/> As Windows que fornece intrínsecos de SSE são suportadas por SSE e SSE2.<br/> \_O XM \_ SSE \_ INTRINSICS não tem nenhum efeito em sistemas que não têm suporte para \_ SSE e SSE2.<br/> Por padrão, \_ xm \_ SSE INTRINSICS é definido quando os usuários são \_ \_ compilados para uma Windows plataforma.<br/> O DirectXMath usa o compilador padrão define ( \_ M \_ IX86 /M AMD64) para determinar Windows \_ \_ destinos x86 ou Windows x64.<br/> |
| \_INTRÍNSECOS \_ DO XM ARM \_ NEON \_\_ | Isso indica que a implementação do DirectXMath usa os intrínsecos arm-NEON. Por padrão, xm ARM NEON INTRINSICS é definido quando os usuários \_ \_ são \_ \_ \_ compilados para um Windows na plataforma ARM/ARM64. O DirectXMath usa a definição do compilador padrão ( \_ M \_ ARM, \_ M \_ ARM64) para determinar esse destino binário.<br/> O suporte a intrínsecos arm-NEON é novo no DirectXMath e não é suportado pelo XNAMath 2.x.<br/>                                                                                                                                                                             |
| \_INTRÍNSECOS \_ XM SSE3 \_\_      | Novo para DirectXMath 3.10. <br/> Quando você especifica essa diretiva do compilador, as funções DirectXMath são implementadas para usar intrínsecos SSE3 quando aplicável; caso contrário, ele usará SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_INTRÍNSECOS \_ XM SSE4 \_\_      | Novidades do DirectMath 3.09. <br/> Quando você especifica essa diretiva do compilador, as funções DirectXMath são implementadas para usar intrínsecos SSE3 e SSE4.1 quando aplicável; caso contrário, ele usará SSE/SSE2. Quando você especifica essa diretiva do compilador, isso também implica INTRÍNSECOS \_ \_ XM SSE3 \_ \_ e \_ \_ INTRÍNSECOS de SSE \_ de XM. \_<br/>                                                                                                                                                                                                                                |
| \_\_INTRÍNSECOS DO AVX \_ XM\_       | Novidades do DirectXMath 3.09. <br/> O uso de /arch:AVX habilita essa diretiva. <br/> Quando você especifica essa diretiva do compilador, as funções DirectXMath são implementadas para usar intrínsecos de SSE3, SSE4.1 e AVX de 128 bits quando aplicável; caso contrário, o DirectXMath usa SSE/SSE2. Quando você especifica essa diretiva do compilador, isso também implica INTRÍNSECOS \_ \_ XM SSE3, \_ \_ XM \_ SSE4 \_ INTRINSICS \_ e XM SSE INTRINSICS \_ e \_ \_ \_ inclui um pequeno subconjunto de instruções SSE3. <br/>                                                                    |
| INTRÍNSECOS DO XM \_ AVX2 \_\_        | Novo para DirectXMath 3.11. <br/> O uso de /arch:AVX2 habilita essa diretiva. Quando você especifica essa diretiva do compilador, as funções DirectXMath usam intrínsecos AVX2, F16C/CVT16, FMA3, AVX de 128 bits, SSE4.1 e SSE3 quando aplicável. Quando você usa INTRÍNSECOS DO XM AVX2 , isso implica INTRÍNSECOS XM F16C, INTRÍNSECOS \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ XM FMA3 , INTRÍNSECOS \_ \_ DE \_ AVX XM, INTRÍNSECOS de \_ SSE XM, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTRÍNSECOS XM SSE3 e INTRÍNSECOS XM SSE4 .<br/>                                                                                       |
| \_INTRÍNSECOS DO XM \_ F16C \_\_      | Novidades do DirectXMath 3.09. <br/> Quando você especifica essa diretiva do compilador, as funções DirectXMath são implementadas para usar intrínsecos SSE3, SSE4.1, AVX de 128 bits e F16C/CVT16 quando aplicável; caso contrário, o DirectXMath usa SSE/SSE2. Quando você usa INTRÍNSECOS XM F16C , isso implica INTRÍNSECOS AVX XM, INTRÍNSECOS de \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SSE \_ \_ \_ XM, \_ INTRÍNSECOS XM SSE3 e INTRÍNSECOS \_ \_ \_ \_ XM SSE4 \_ \_ .<br/>                                                                                                                                                 |
| \_INTRÍNSECOS DO XM \_ FMA3 \_\_      | Novo para DirectXMath 3.11. <br/> Quando você especificar essa diretiva do compilador, as funções DirectXMath usarão intrínsecos SSE3, SSE4.1, AVX de 128 bits e FMA3 quando aplicável; caso contrário, o DirectXMath usa SSE/SSE2. Quando você usa INTRÍNSECOS XM FMA3 , isso implica INTRÍNSECOS AVX XM, INTRÍNSECOS de \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SSE XM, \_ INTRÍNSECOS XM SSE3 e INTRÍNSECOS \_ \_ \_ XM \_ SSE4 \_ \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Isso permite o uso da convenção \_ \_ de chamada vectorcall para Windows x86 ou Windows x64. Ele assume como padrão \_ XM \_ VECTORCALL \_ =1 quando o compilador dá suporte a esse recurso. Você pode defini-lo manualmente como \_ XM \_ VECTORCALL \_ =0 para sempre desabilitá-lo. <br/> \_\_Vectorcall não tem suporte para o Windows na plataforma ARM/ARM64 ou no C++Gerenciado. <br/>                                                                                                                                                                                                                 |
| \_INTRÍNSECOS \_ XM SVML \_\_     | Novo para DirectXMath 3.16. <br/> Com o VS 2019 ou posterior, isso permite que a biblioteca use a Biblioteca de Matrizes de Vetor Curto da Intel &reg; para x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
