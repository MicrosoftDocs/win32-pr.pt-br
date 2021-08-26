---
title: Os arquivos IDL e ACF
description: A sintaxe do linguagem IDL da Microsoft (MIDL) baseia-se na sintaxe da linguagem de programação C. Quando um conceito de linguagem nesta descrição de MIDL não está totalmente definido, a definição de linguagem C desse termo é implícita.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- Chamada de procedimento remoto RPC, descrito, IDL e ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788756c6762575d2366950f1b6412a76c03d14518acb1707dfdaf109ba2b5fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017096"
---
# <a name="the-idl-and-acf-files"></a>Os arquivos IDL e ACF

A sintaxe do linguagem IDL da Microsoft (MIDL) baseia-se na sintaxe da linguagem de programação C. Quando um conceito de linguagem nesta descrição de MIDL não está totalmente definido, a definição de linguagem C desse termo é implícita.

O design MIDL Especifica dois arquivos distintos: o arquivo IDL (Interface Definition Language) e o arquivo de configuração de aplicativo (ACF). Esses arquivos contêm atributos que direcionam a geração dos arquivos stub de linguagem C que gerenciam a chamada de procedimento remoto (RPC). O arquivo IDL contém uma descrição da interface entre o cliente e os programas do servidor. Os aplicativos RPC usam o arquivo ACF para descrever as características da interface que são específicas para o hardware e o sistema operacional que compõem um ambiente operacional específico. A finalidade de dividir essas informações em dois arquivos é manter a interface do software separada das características que afetam apenas o ambiente operacional.

O arquivo IDL especifica um contrato de rede entre o cliente e o servidor, ou seja, o arquivo IDL especifica o que é transmitido entre o cliente e o servidor. Manter essas informações diferentes das informações sobre o ambiente operacional torna o arquivo IDL portátil para outros ambientes. O arquivo IDL consiste em duas partes: um [cabeçalho de interface](the-idl-interface-header.md) e um [corpo de interface](the-idl-interface-body.md).

O ACF especifica atributos que afetam apenas o desempenho local em vez do contrato de rede. O Microsoft RPC permite combinar os atributos ACF e IDL em um único arquivo IDL. Você também pode combinar várias interfaces em um único arquivo IDL (e seu ACF).

Esta seção resume os atributos que são especificados nos arquivos IDL e ACF. Ele se destina a fornecer apenas uma visão geral. Para obter informações mais detalhadas, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference)e a [referência de Command-Line MIDL](/windows/desktop/Midl/midl-command-line-reference). A discussão nesta seção é apresentada nos seguintes tópicos:

-   [O arquivo IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [O arquivo de configuração de aplicativo (ACF)](the-application-configuration-file-acf-.md)
-   [Saída do compilador MIDL](midl-compiler-output.md)

 

 