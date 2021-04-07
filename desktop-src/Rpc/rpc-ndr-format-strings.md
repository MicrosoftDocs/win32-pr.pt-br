---
title: Cadeias de caracteres de formato NDR de RPC
description: Cadeias de caracteres de formato NDR RPC (chamada de procedimento remoto).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0569a913d6c5a4b19b342cc288d6a8682dfc4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823952"
---
# <a name="rpc-ndr-format-strings"></a>Cadeias de caracteres de formato NDR de RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Mecanismo de NDR: intérprete de 32 bits

Este documento descreve os descritores de cadeia de caracteres de formato, às vezes chamados de MOPs, para o mecanismo NDR de 32 bits. Esta seção descreve as alterações associadas à evolução do intérprete [**– Oi**](/windows/desktop/Midl/-oi) para a camada de intérprete **– OIF** , bem como adições relacionadas a pipes e suporte assíncrono.

Este documento descreve a tecnologia de linguagem IDL da Microsoft (MIDL) atual da perspectiva do mecanismo e o mecanismo de NDR atual.

## <a name="overview"></a>Visão geral

O mecanismo NDR é o mecanismo de marshaling dos componentes RPC (chamada de procedimento remoto) e DCOM. Ele lida com todos os problemas relacionados a stub de uma chamada remota. Como um processo, o marshaling de NDR é controlado pelo código C de stubs gerados por MIDL, um gerador de tipo JIT de MIDL ou por stubs gerados por outras ferramentas ou gravados manualmente. Por sua vez, o mecanismo de NDR orienta o tempo de execução subjacente (DCOM ou RPC) que se comunica com transportes específicos.

O objetivo original do design era fornecer uma ferramenta para o marshaling eficaz de dados arbitrários, com base nas informações fornecidas pelo compilador MIDL. As cadeias de caracteres de formato descritas neste documento — e, de fato, todas as informações geradas pelo compilador para consumo do mecanismo de NDR — sempre foram consideradas uma interface interna entre o compilador e o mecanismo. Da mesma forma, as interfaces disponíveis para o mecanismo para lidar com os problemas de tempo de execução também são internas (algumas exceções existem no lado do tempo de execução RPC e algumas interfaces DCOM usadas pelo mecanismo são externas).

Duas abordagens típicas ao marshaling sempre foram embutidas e a tecnologia controlada por dados (interpretada). O MIDL dá suporte a ambos por meio de suas opções [**– os**](/windows/desktop/Midl/-os) e [**– Oi \***](/windows/desktop/Midl/-oi) em seus stubs gerados por C. Além disso, o MIDL pode gerar as bibliotecas de TLB usadas pelo pacote oleautomation. Da mesma forma, uma perspectiva dos internos do mecanismo é que ele consiste em duas partes.

O primeiro é um conjunto de rotinas que manipulam o dimensionamento, o marshaling e assim por diante, correspondendo a objetos de tipo de dados típicos, como uma estrutura ou uma matriz. Essas rotinas são ajustadas para o desempenho; por exemplo, eles normalmente tentam bloquear a cópia de dados sempre que possível. Essa parte é geralmente conhecida como o mecanismo de NDR principal.

A segunda parte consiste em um intérprete e suas partes relacionadas. O intérprete usa rotinas do mecanismo NDR principal, como se fosse de uma biblioteca interna, a fim de executar uma chamada remota com todos os seus argumentos com marshaling e sem marshaling, conforme apropriado.

O mecanismo NDR principal é usado de forma semelhante, seja usado de stubs embutidos ou do intérprete. Todas as rotinas do mecanismo principal dependem do estado passado por uma estrutura de mensagem de stub. A estrutura é configurada adequadamente pelo stub embutido ou pelo intérprete. Ao longo dos anos, o mecanismo principal tinha sido usado em um contexto diferente; Atualmente, o intérprete é, na verdade, um conjunto de vários loops distintos do interpretador. Eles estão relacionados aos interpretadores antigos e novos ([**– Oi**](/windows/desktop/Midl/-oi) versus **– OIF**), bem como a loops relacionados à serialização de dados (seleção), ao suporte assíncrono de RPC e ao suporte assíncrono de DCOM (RPC e DCOM têm modelos de programação assíncrona diferentes).

Além da adição de novos recursos, um aspecto importante da evolução do mecanismo de NDR é uma mudança geral na abordagem para os interpretadores. O NDR versão 1.1 começou como parte de uma nova abordagem MIDL 2,0 para realizar o marshaling, com os stubs embutidos sendo preferidos para considerações de desempenho. Com a versão mais recente do NDR, [**– OIF**](/windows/desktop/Midl/-oi) tornou-se o modo mais amplamente usado do compilador, quase a exclusão de stubs embutidos.

Os descritores de cadeia de caracteres de formato do mecanismo NDR RPC são descritos mais detalhadamente nos seguintes tópicos:

-   [Cadeias de caracteres de formato](format-strings.md)
-   [Cadeias de caracteres de formato de procedimento](procedure-format-strings.md)
-   [Descritor de cabeçalho de procedimento](procedure-header-descriptor.md)
-   [Alças](handles.md)
-   [O cabeçalho](the-header.md)
-   [Descritores de parâmetro](parameter-descriptors.md)
-   [Cadeias de formato de tipo](type-format-strings.md)

 

 