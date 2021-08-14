---
title: Cadeias de caracteres de formato NDR RPC
description: Cadeias de caracteres de formato NDR de RPC (Chamada de Procedimento Remoto).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a481e2c992f3fd4dda2d5552fbbabb7e9b01e6eb639a092e25ba9a26bd59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926300"
---
# <a name="rpc-ndr-format-strings"></a>Cadeias de caracteres de formato NDR RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Mecanismo NDR: Interpretador de 32 bits

Este documento descreve os descritores de cadeia de caracteres de formato, às vezes chamados de MOPs, para o mecanismo NDR de 32 bits. Esta seção descreve as alterações associadas à evolução do interpretador [**–Oi**](/windows/desktop/Midl/-oi) para a camada do interpretador **–Oif,** bem como adições relacionadas a pipes e suporte assíncrono.

Este documento descreve a tecnologia MIDL (linguagem IDL da Microsoft atual) da perspectiva do mecanismo e o mecanismo NDR atual.

## <a name="overview"></a>Visão geral

O mecanismo NDR é o mecanismo de marshaling dos componentes RPC (Chamada de Procedimento Remoto) e DCOM. Ele lida com todos os problemas relacionados ao stub de uma chamada remota. Como um processo, o marshaling de NDR é orientado pelo código C de stubs gerados por MIDL, um gerador de tipo JIT MIDL ou por stubs gerados por outras ferramentas ou gravados manualmente. Por sua vez, o mecanismo NDR orienta o DCOM (ou RPC) subjacente que se comunica com transporte específico.

A meta original do design era fornecer uma ferramenta para marshaling efetivo para dados arbitrários, com base nas informações fornecidas pelo compilador MIDL. As cadeias de caracteres de formato descritas neste documento e, na verdade, todas as informações geradas pelo compilador para consumo do mecanismo NDR sempre foram consideradas uma interface interna entre o compilador e o mecanismo. Da mesma forma, as interfaces disponíveis para o mecanismo lidar com problemas de tempo de run-time também são principalmente internas (algumas exceções existem no lado do tempo de executar RPC e algumas interfaces DCOM usadas pelo mecanismo são externas).

Duas abordagens típicas para marshaling sempre foram em linha e tecnologia controlada por dados (interpretada). O MIDL dá suporte a ambos por meio de suas opções [**–Os**](/windows/desktop/Midl/-os) e [**–Oi \***](/windows/desktop/Midl/-oi) em seus stubs gerados por C. Além disso, MIDL pode gerar as bibliotecas TLB usadas pelo pacote oleautomation. Da mesma forma, uma perspectiva dos componentes internos do mecanismo é que ele consiste em duas partes.

A primeira é um conjunto de rotinas que lidam com o ressaramento, marshaling e assim por diante, correspondentes a objetos de tipo de dados típicos, como uma estrutura ou uma matriz. Essas rotinas são ajustadas para o desempenho; por exemplo, eles normalmente tentam bloquear a cópia de dados sempre que possível. Essa parte geralmente é conhecida como o mecanismo NDR principal.

A segunda parte consiste em um interpretador e suas partes relacionadas. O interpretador usa rotinas do mecanismo NDR principal, como se fosse de uma biblioteca interna, para executar uma chamada remota com todos os seus argumentos empacotados e não empacotados, conforme apropriado.

O mecanismo NDR principal é usado de maneira semelhante, seja usado de stubs em linha ou do interpretador. Todas as rotinas principais do mecanismo dependem do estado passado por uma estrutura de mensagem de stub. A estrutura é configurada adequadamente pelo stub em linha ou pelo interpretador. Ao longo dos anos, o mecanismo principal foi usado em um contexto diferente; atualmente, o interpretador é, na verdade, um conjunto de vários loops de interpretador distintos. Eles estão relacionados aos interpretadores antigos e novos ([**–Oi**](/windows/desktop/Midl/-oi) versus **–Oif),** bem como a loops relacionados à serialização de dados (seleção), suporte a RPC assíncrono e suporte assíncrono DCOM (RPC e DCOM têm diferentes modelos de programação assíncrona).

Além da adição de novos recursos, um aspecto importante da evolução do mecanismo NDR é uma mudança geral na abordagem para interpretador. A NDR versão 1.1 começou como parte de uma nova abordagem MIDL 2.0 para marshaling, com os stubs em linha sendo preferenciais para considerações de desempenho. Com a versão mais recente do NDR, [**–Oif**](/windows/desktop/Midl/-oi) se tornou o modo mais amplamente usado do compilador, quase à exclusão de stubs em linha.

Descritores de cadeia de caracteres de formato do Mecanismo NDR RPC são descritos mais detalhadamente nos tópicos a seguir:

-   [Cadeias de caracteres de formato](format-strings.md)
-   [Cadeias de caracteres de formato de procedimento](procedure-format-strings.md)
-   [Descritor de header de procedimento](procedure-header-descriptor.md)
-   [Alças](handles.md)
-   [O header](the-header.md)
-   [Descritores de parâmetro](parameter-descriptors.md)
-   [Cadeias de caracteres de formato de tipo](type-format-strings.md)

 

 