---
title: Ferramenta de Command-Line de JActiveX
description: O aplicativo de linha de comando JActiveX é um componente do Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105815545"
---
# <a name="jactivex-command-line-tool"></a>Ferramenta de Command-Line de JActiveX

O aplicativo de linha de comando JActiveX é um componente do Visual J++ 6,0. Ele lê a biblioteca de tipos de um controle ActiveX da Microsoft e gera os arquivos de origem Java correspondentes. Em seguida, você pode compilar esses arquivos de origem e importá-los para seu aplicativo Java.

Para gerar arquivos de origem Java para um objeto COM, no prompt de comando, execute:

 *nome de arquivo* Jactivex

em que *filename* é o nome do arquivo que contém a biblioteca de tipos. Esse arquivo pode ter qualquer uma das seguintes extensões de nome de arquivo:. tlb,. olb,. ocx,. dll ou. exe.

Para obter mais informações sobre os parâmetros opcionais que podem ser definidos em JActiveX, consulte a documentação do Visual J++ ou digite a seguinte linha de comando:

**jactivex /?**

> [!WARNING]
> Não use compiladores do Visual J++ antes da versão 1.02.3920 para compilar os arquivos gerados pelo JActiveX.exe. Isso ocorre porque os arquivos de origem gerados devem ser compilados com um @com-aware compilador. Somente os compiladores do Visual J++ posteriores à versão 1.02.3920 são @com-aware .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




