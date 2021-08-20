---
title: Ferramenta de Command-Line de JavaTLB
description: Ferramenta de Command-Line de JavaTLB
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ade0a20a1c41310422c08310f2d0534914993d79909f51990c48aa04df0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918620"
---
# <a name="javatlb-command-line-tool"></a>Ferramenta de Command-Line de JavaTLB

JavaTLB é um componente do Visual J++ 5,0. JavaTLB é um aplicativo de linha de comando que gera arquivos de classe para um objeto COM. Os métodos que contêm tipos de dados que não podem ser representados de forma precisa e segura em Java não são convertidos.

Diferentemente do [Assistente da biblioteca de tipos Java](java-type-library-wizard.md), o JavaTLB não gera um arquivo de resumo contendo as informações da biblioteca de tipos do Java.

Para gerar arquivos de classe Java para um único objeto COM, a partir do prompt de comando, execute:

 *nome de arquivo* javatlb

em que *filename* é o nome do arquivo que contém a biblioteca de tipos. Esse arquivo pode ter qualquer uma das seguintes extensões de nome de arquivo:. tlb,. olb,. ocx, .dll ou .exe.

Para gerar arquivos de classe Java para vários objetos COM, a partir do prompt de comando, execute:

**javatlb @**_textfile_

em que *textfile* é o nome de um arquivo de texto que contém uma lista dos arquivos que contêm as bibliotecas de tipos do objeto com.

> [!Note]  
> No Visual J++ 6,0, a ferramenta de linha de comando JavaTLB é substituída pela [ferramenta Jactivex](jactivex-command-line-tool.md). Para obter mais informações, consulte a documentação do Visual J++ 6,0.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




