---
title: Ferramenta de Command-Line JActiveX
description: O aplicativo de linha de comando JActiveX é um componente do Visual J++ 6.0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae611e56c44b78398817cd0c78804d343fa97754f80fb3b036ea2705c801070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992646"
---
# <a name="jactivex-command-line-tool"></a>Ferramenta de Command-Line JActiveX

O aplicativo de linha de comando JActiveX é um componente do Visual J++ 6.0. Ele lê a biblioteca de tipos de um controle microsoft ActiveX e gera os arquivos de origem Java correspondentes. Em seguida, você pode compilar esses arquivos de origem e importá-los para seu aplicativo Java.

Para gerar arquivos de origem Java para um objeto COM, no prompt de comando, execute:

**jactivex** *filename*

em *que filename* é o nome do arquivo que contém a biblioteca de tipos. Esse arquivo pode ter qualquer uma das seguintes extensões de nome de arquivo: .tlb, .olb, .ocx, .dll ou .exe.

Para obter mais informações sobre os parâmetros opcionais que você pode definir em JActiveX, consulte a documentação do Visual J++ ou digite a seguinte linha de comando:

**jactivex /?**

> [!WARNING]
> Não use compiladores do Visual J++ antes da versão 1.02.3920 para compilar os arquivos gerados pelo JActiveX.exe. Isso porque os arquivos de origem gerados devem ser compilados com um @com-aware compilador. Somente compiladores do Visual J++ posteriores à versão 1.02.3920 são @com-aware .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Traduzindo para Java](translating-to-java.md)
</dt> </dl>

 

 




