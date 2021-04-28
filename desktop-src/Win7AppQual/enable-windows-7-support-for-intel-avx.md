---
description: Habilitar o suporte do Windows 7 para Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitar o suporte do Windows 7 para Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1509bac62634c85aa733b2c1de0c152169ac6cda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088454"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Habilitar o suporte do Windows 7 para Intel AVX

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** -Windows 7 SP1  
**Servidores** -Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

Intel<sup>?</sup> Extensões de vetor avançadas (AVX)<sup>?</sup> é uma extensão de vetor de ponto flutuante de 256-bit SIMD da arquitetura Intel. Ele inclui extensões para os conjuntos de instruções e de registro.

A Microsoft desenvolveu alguns aprimoramentos de API, como o XState functions, que permitem que os aplicativos acessem e manipulem informações e estado do recurso do processador estendido, incluindo AVX.

## <a name="usage-scenarios"></a>Cenários de uso

Há três níveis gerais de impacto potencial.

**Nível 1:** Os aplicativos que não usam o Intel AVX diretamente não verão nenhum impacto sobre sua funcionalidade, mesmo que eles chamem em bibliotecas ou usem compiladores que usam indiretamente ou gerem extensões Intel AVX. Isso representa, de longe, a maioria dos aplicativos.

**Nível 2:** Os aplicativos avançados que usam explicitamente o conjunto de instruções Intel AVX poderão acessar e alterar o conteúdo do registro do AVX quando uma exceção de hardware for gerada. Um número muito pequeno de aplicativos se enquadraria nessa categoria, pois implica um conhecimento profundo do fluxo de instrução em execução no momento da exceção, como aplicativos com seções escritas em linguagem de assembly ou aqueles que geram código de máquina em tempo de execução (por exemplo, tempos de execução de código gerenciado com compilação just-in-time).

**Nível 3:** Os aplicativos do depurador poderão acessar e manipular o estado AVX no aplicativo que está sendo depurado.

## <a name="how-to-leverage-feature-capabilities"></a>Como aproveitar os recursos de recursos

**Nível 1:** Nenhuma ação é necessária para que os aplicativos usem o Intel AVX.

**Nível 2:** Os aplicativos nessa categoria têm a opção de acessar e manipular o estado AVX no momento da exceção de dentro de seus filtros de exceção. Depois de obter o contexto do processador base via GetExceptionInformation, os filtros devem:

 **1.** Verifique o valor do sinalizador **\_ XSTATE do contexto** . Esse sinalizador indica a presença de pelo menos um recurso XState no contexto.  
**2.** se esse for o caso, chame **GetXStateFeaturesMask** e teste o valor do sinalizador **XSTATE \_ AVX** na máscara retornada. Isso indica a presença do estado AVX no contexto.  
**3.** chame **LocateXStateFeature** para recuperar o local real onde o estado AVX está armazenado.  

**Nível 3:** Não é necessário atualizar os aplicativos de depurador existentes, a menos que desejem acessar os registros do Intel AVX:

**1.** para determinar se o AVX está habilitado, o depurador deve usar:

-   GetEnabledXStateFeatures para obter uma máscara de recursos de XState habilitados em processadores x86 ou x64 para determinar quais recursos estão presentes e habilitados no sistema antes de usar um recurso de processador XState ou tentar manipular os contextos XState

  
**2.** se AVX estiver presente e você desejar recuperar e manipular o estado AVX do aplicativo que está sendo depurado (por exemplo, GetThreadContext e SetThreadContext), o depurador deverá usar:

-   Função InitializeContext para inicializar uma estrutura de contexto dentro de um buffer com o tamanho e o alinhamento necessários
-   Função CopyContext para copiar uma estrutura de contexto de origem (incluindo qualquer XState) em uma estrutura de contexto de destino inicializada

  
**3.** para testar, definir e localizar o estado AVX dentro de um contexto de processador, o depurador deve usar:

-   LocateXStateFeature para recuperar um ponteiro para o estado do processador para um recurso de XState individual dentro de uma estrutura de contexto
-   GetXStateFeaturesMask para retornar a máscara do conjunto de recursos do XState em uma estrutura de contexto
-   SetXStateFeaturesMask para definir a máscara do conjunto de recursos do XState em uma estrutura de contexto

  


## <a name="links-to-other-resources"></a>Links para outros recursos

-   Para obter informações sobre as funções XState no SDK do Windows, consulte [Debugging Functions](../debug/debugging-functions.md).
-   Para obter uma visão geral das instruções e dos recursos do Intel AVX, consulte [Intel AVX: novas fronteiras em melhorias de desempenho e eficiência energética](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
