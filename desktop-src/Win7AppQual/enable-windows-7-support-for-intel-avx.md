---
description: Habilitar Windows 7 para Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitar Windows 7 para Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30469d0218f5da2c9f6df2b4f5637edffe09153ebad721f48b47401ecb1f3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329810"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Habilitar Windows 7 para Intel AVX

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** – Windows 7 SP1  
**Servidores** – Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Baixa  





## <a name="description"></a>Descrição

Intel<sup>?</sup> Extensões avançadas de vetor (AVX)<sup>?</sup> é uma extensão de vetor de ponto flutuante SIMD de 256 bits da arquitetura Intel. Ele inclui extensões para conjuntos de instruções e registros.

A Microsoft desenvolveu algumas melhorias de API, como funções XState, que permitem que os aplicativos acessem e manipulem informações e estado de recursos do processador estendido, incluindo AVX.

## <a name="usage-scenarios"></a>Cenários de uso

Há três níveis gerais de impacto potencial.

**Nível 1:** Os aplicativos que não usam o Intel AVX diretamente não verão nenhum impacto em sua funcionalidade, mesmo se chamarem em bibliotecas ou usarem compiladores que usam indiretamente ou geram extensões Intel AVX. Isso representa de longe a maioria dos aplicativos.

**Nível 2:** Os aplicativos avançados que usam explicitamente o conjunto de instruções Intel AVX poderão acessar e alterar o conteúdo do registro AVX quando uma exceção de hardware for gerado. Um número muito pequeno de aplicativos se enquadraria nessa categoria, pois isso implica um conhecimento profundo do fluxo de instruções em execução no momento da exceção, como aplicativos com seções escritas em linguagem de assembly ou aqueles que geram código de computador em runtime (por exemplo, runtimes de código gerenciado com compilação just-in-time).

**Nível 3:** Os aplicativos de depurador poderão acessar e manipular o estado AVX no aplicativo que está sendo depurado.

## <a name="how-to-leverage-feature-capabilities"></a>Como aproveitar os recursos

**Nível 1:** Nenhuma ação é necessária para que os aplicativos usem o Intel AVX.

**Nível 2:** Os aplicativos nessa categoria têm a opção de acessar e manipular o estado AVX no momento da exceção de dentro de seus filtros de exceção. Depois de obter o contexto do processador base por meio de GetExceptionInformation, os filtros devem:

 **1.** Verifique o valor do sinalizador **CONTEXT \_ XSTATE.** Esse sinalizador indica a presença de pelo menos um recurso XState no contexto.  
**2.** Se esse for o caso, chame **GetXStateFeaturesMask** e teste o valor do sinalizador **\_ AVX XSTATE** na máscara retornada. Isso indica a presença do estado AVX no contexto.  
**3.** Chame **LocateXStateFeature** para recuperar o local real em que o estado AVX está armazenado.  

**Nível 3:** Não é necessário atualizar aplicativos de depurador existentes, a menos que eles desejem acessar os registros intel AVX:

**1.** Para determinar se o AVX está habilitado, o depurador deve usar:

-   GetEnabledXStateFeatures para obter uma máscara de recursos XState habilitados em processadores x86 ou x64 para determinar quais recursos estão presentes e habilitados no sistema antes de usar um recurso de processador XState ou tentar manipular contextos XState

  
**2.** Se AVX estiver presente e você quiser recuperar e manipular o estado AVX do aplicativo que está sendo depurado (por exemplo, GetThreadContext e SetThreadContext), o depurador deverá usar:

-   Função InitializeContext para inicializar uma estrutura de contexto dentro de um buffer com o tamanho e o alinhamento necessários
-   Função CopyContext para copiar uma estrutura de contexto de origem (incluindo qualquer XState) em uma estrutura de contexto de destino inicializada

  
**3.** Para testar, definir e localizar o estado AVX dentro de um contexto de processador, o depurador deve usar:

-   LocateXStateFeature para recuperar um ponteiro para o estado do processador para um recurso XState individual dentro de uma estrutura de contexto
-   GetXStateFeaturesMask para retornar a máscara de recursos XState definida em uma estrutura de contexto
-   SetXStateFeaturesMask para definir a máscara de recursos XState definida em uma estrutura de contexto

  


## <a name="links-to-other-resources"></a>Links para outros recursos

-   Para obter informações sobre as funções XState no SDK Windows, consulte [Funções de depuração](../debug/debugging-functions.md).
-   Para obter uma visão geral das instruções e funcionalidades do Intel AVX, consulte [Intel AVX: New Improvements in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
