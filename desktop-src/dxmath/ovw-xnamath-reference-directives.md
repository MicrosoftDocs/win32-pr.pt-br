---
description: As diretivas do compilador ajustam a funcionalidade que a biblioteca DirectXMath usa.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Diretivas do compilador da biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f1d67ecd4772116a3bf29f802c39b2e348fd5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763023"
---
# <a name="directxmath-library-compiler-directives"></a>Diretivas do compilador da biblioteca DirectXMath

As diretivas do compilador ajustam a funcionalidade que a biblioteca DirectXMath usa.



| Diretiva                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ não \_ intrínsecos\_        | Quando \_ XM \_ nenhum \_ intrínseco \_ é definido, as operações de DirectXMath são implementadas sem usar nenhum intrínsecor específico da plataforma. Em vez disso, DirectXMath usa apenas operações de ponto flutuante padrão.<br/> Por padrão, \_ XM \_ nenhum \_ intrínseco \_ não está definido.<br/> Essa diretiva substitui todas as outras diretivas. Portanto, recomendamos que você verifique \_ XM \_ não \_ intrínsecos \_ antes de determinar o status de \_ XM \_ ARM \_ Neon \_ intrínsecos \_ ou \_ XM \_ SSE \_ intrínsecos \_ .<br/>                                                                              |
| \_\_intrínsecos do XM SSE \_\_       | Quando \_ XM \_ SSE \_ intrínsecos \_ é definido, o código é compilado para usar o suporte a SSE e SSE2 em plataformas que dão suporte a esses conjuntos de instruções.<br/> As versões do Windows que fornecem o SSE intrínsecos dão suporte a SSE e SSE2.<br/> \_O XM \_ SSE \_ intrínsecos não \_ tem efeito em sistemas que não dão suporte a SSE e SSE2.<br/> Por padrão, o \_ XM \_ SSE \_ intrínsecos \_ é definido quando os usuários são compilados para uma plataforma Windows.<br/> O DirectXMath usa o compilador padrão define ( \_ M \_ IX86/ \_ m \_ AMD64) para determinar os destinos do Windows x86 ou do Windows x64.<br/> |
| \_XM \_ ARM \_ Neon \_ intrínsecos\_ | Isso indica os usos de implementação de DirectXMath dos intrínsecos ARM-NEON. Por padrão, o \_ XM \_ ARM \_ Neon \_ intrínsecos \_ é definido quando os usuários são compilados para uma plataforma Windows RT. DirectXMath usa o compilador padrão define ( \_ m \_ ARM, \_ m \_ ARM64) para determinar esse destino binário.<br/> O suporte do ARM-NEON intrínsecos é novo no DirectXMath e não tem suporte do XNAMath 2. x.<br/>                                                                                                                                                                             |
| \_XM \_ SSE3 \_ intrínsecos\_      | Novo para o SDK de atualização do Windows 10 para criadores. <br/> Quando você especifica essa diretiva de compilador, as funções DirectXMath são implementadas para fazer uso de intrínsecos SSE3 quando aplicável; caso contrário, ele usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_XM \_ SSE4 \_ intrínsecos\_      | Novo para o SDK de aniversário do Windows 10.<br/> Quando você especifica essa diretiva de compilador, as funções DirectXMath são implementadas para fazer uso de intrínsecos SSE3 e SSE 4.1 quando aplicável; caso contrário, ele usa SSE/SSE2. Quando você especifica essa diretiva de compilador, ela também implica \_ XM \_ SSE3 \_ intrínsecos \_ e \_ XM \_ SSE \_ intrínsecos \_ .<br/>                                                                                                                                                                                                                                |
| \_XM \_ AVX \_ intrínsecos\_       | Novo para o SDK de aniversário do Windows 10.<br/> Uso de/Arch: AVX habilitará essa diretiva. <br/> Quando você especifica essa diretiva de compilador, as funções DirectXMath são implementadas para fazer uso de SSE3, SSE 4.1 e AVX de 128 bits intrínsecos quando aplicável; caso contrário, DirectXMath usará SSE/SSE2. Quando você especifica essa diretiva de compilador, ela também implica \_ XM \_ SSE3 \_ intrínsecos, \_ XM \_ SSE4 \_ intrínsecos \_ e \_ XM \_ SSE \_ intrínsecos \_ e inclui um pequeno subconjunto de instruções de SSE3. <br/>                                                                    |
| XM \_ AVX2 \_ intrínsecos\_        | Novo para o SDK de atualização do Windows 10 outono Creators<br/> Uso de/Arch: AVX2 habilita essa diretiva. Quando você especifica essa diretiva de compilador, as funções DirectXMath usam AVX2, F16C/CVT16, FMA3, AVX 128-bit, SSE 4.1 e SSE3 intrínsecos quando aplicável. Quando você usa \_ XM \_ AVX2 \_ intrínsecos \_ , ele implica \_ XM \_ F16C \_ intrínsecos \_ , \_ XM \_ FMA3 \_ intrínsecos \_ , \_ XM \_ AVX \_ intrínsecos \_ , \_ XM \_ SSE \_ intrínsecos \_ , \_ XM \_ SSE3 \_ intrínsecos \_ e \_ XM \_ \_ intrínsecos SSE4 \_ .<br/>                                                                                       |
| \_XM \_ F16C \_ intrínsecos\_      | Novo para o SDK de aniversário do Windows 10.<br/> Quando você especifica essa diretiva de compilador, as funções DirectXMath são implementadas para fazer uso de SSE3, SSE 4.1, AVX 128-bit e F16C/CVT16 intrínsecos quando aplicável; caso contrário, DirectXMath usará SSE/SSE2. Quando você usa \_ XM \_ F16C \_ intrínsecos \_ , ele implica \_ XM \_ AVX \_ intrínsecos \_ , \_ XM \_ SSE \_ intrínsecos \_ , \_ XM \_ SSE3 \_ intrínsecos \_ e \_ XM \_ \_ intrínsecos SSE4 \_ .<br/>                                                                                                                                                 |
| \_XM \_ FMA3 \_ intrínsecos\_      | Novo para o SDK de atualização do Windows 10 outono Creators<br/> Quando você especifica essa diretiva de compilador, as funções de DirectXMath farão uso de SSE3, SSE 4.1, AVX de 128 bits e de FMA3 intrínsecos quando aplicável; caso contrário, DirectXMath usará SSE/SSE2. Quando você usa \_ XM \_ FMA3 \_ intrínsecos \_ , ele implica \_ XM \_ AVX \_ intrínsecos \_ , \_ XM \_ SSE \_ intrínsecos \_ , \_ XM \_ SSE3 \_ intrínsecos \_ e \_ XM \_ \_ intrínsecos SSE4 \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Isso permite o uso da nova \_ \_ Convenção de chamada vectorcall para destinos Windows x86 ou Windows x64. O padrão é \_ XM \_ VECTORCALL \_ = 1 quando o compilador dá suporte a esse recurso. Você pode defini-lo manualmente como \_ XM \_ VECTORCALL \_ = 0 para sempre desabilitá-lo. <br/> \_\_vectorcall não tem suporte para a plataforma Windows RT ou C++ gerenciado. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 




