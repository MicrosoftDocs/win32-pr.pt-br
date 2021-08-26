---
title: Arquivos IDL
description: Arquivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e2329d14ea844658bf9ad08927ddcef5067debed7a1c8a424c06d3c7adb8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992896"
---
# <a name="idl-files"></a>Arquivos IDL

O COM usa o linguagem IDL da Microsoft (MIDL) para descrever objetos COM. MIDL é uma extensão da IDL para ambientes de computação distribuídos definidos pelo Open Software Foundation, que foi desenvolvido para definir interfaces para chamadas de procedimento remoto em aplicativos cliente/servidor tradicionais. MIDL inclui a maioria dos atributos e instruções da ODL (Linguagem de Definição de Objeto), a linguagem originalmente usada para gerar bibliotecas de tipos para a Automação OLE.

Em C++ e Java, um desenvolvedor que cria um objeto COM cria um arquivo IDL que o compilador MIDL processa para criar uma biblioteca de tipos, arquivos de header e proxy ou ambos. Uma *biblioteca de* tipos é um arquivo binário que descreve o objeto COM ou interfaces COM ou ambos. Uma biblioteca de tipos é a versão compilada do arquivo IDL. No entanto, as bibliotecas de tipos só suportam semântica ODL. Em particular, eles não podem representar todas as informações de um arquivo IDL relacionado a atributos IDL, como \[ [**size \_ é**](/windows/desktop/Midl/size-is) \] . Você precisa criar e usar arquivos proxy para arquivos IDL afetados pela perda de informações na biblioteca de tipos.

No Visual Basic, um desenvolvedor que cria um objeto COM não cria um arquivo IDL. Em vez disso, Visual Basic coleta informações usando propriedades de classe e projeto e cria diretamente a biblioteca de tipos.

 

 