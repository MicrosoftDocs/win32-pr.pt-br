---
title: Arquivos IDL
description: Arquivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824011"
---
# <a name="idl-files"></a>Arquivos IDL

COM usa o linguagem IDL da Microsoft (MIDL) para descrever objetos COM. MIDL é uma extensão da IDL para ambientes de computação distribuídos definidos pela Open Software Foundation, que foi desenvolvida para definir interfaces para chamadas de procedimento remotas em aplicativos cliente/servidor tradicionais. MIDL inclui a maioria dos atributos e instruções do ODL (linguagem de definição de objeto), a linguagem usada originalmente para gerar bibliotecas de tipos para automação OLE.

Em C++ e Java, um desenvolvedor criando um objeto COM cria um arquivo IDL que o compilador MIDL processa para criar uma biblioteca de tipos ou um cabeçalho e arquivos de proxy, ou ambos. Uma *biblioteca de tipos* é um arquivo binário que descreve o objeto com ou interfaces com, ou ambos. Uma biblioteca de tipos é a versão compilada do arquivo IDL. No entanto, as bibliotecas de tipos dão suporte apenas à semântica ODL. Em particular, eles não podem representar todas as informações de um arquivo IDL relacionado a atributos IDL, como o \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) \] . Você precisa criar e usar arquivos de proxy para arquivos IDL afetados pela perda de informações na biblioteca de tipos.

No Visual Basic, um desenvolvedor que cria um objeto COM não cria um arquivo IDL. Em vez disso, Visual Basic coleta informações usando propriedades de classe e projeto e cria diretamente a biblioteca de tipos.

 

 