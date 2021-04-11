---
description: Configurar símbolos corretamente para depuração pode ser uma tarefa desafiadora, especialmente para a depuração de kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: '{1&gt;{2&gt;Servidor e repositórios de símbolos&lt;2}&lt;1}'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163980"
---
# <a name="symbol-server-and-symbol-stores"></a>{1&gt;{2&gt;Servidor e repositórios de símbolos&lt;2}&lt;1}

Configurar símbolos corretamente para depuração pode ser uma tarefa desafiadora, especialmente para a depuração de kernel. Geralmente, é necessário que você conheça os nomes e as versões de todos os produtos em seu computador. O depurador deve ser capaz de localizar os arquivos de símbolo que correspondem a cada versão do produto e service pack. Isso pode resultar em um caminho de símbolo muito longo que consiste em uma longa lista de diretórios.

Para simplificar essas dificuldades na coordenação de arquivos de símbolo, use o *servidor de símbolos*. O servidor de símbolos permite que os depuradores recuperem automaticamente os arquivos de símbolo corretos sem nomes de produtos, versões ou números de Build. As ferramentas de depuração para Windows contêm o servidor de símbolos SymSrv.

O servidor de símbolos é ativado incluindo uma determinada cadeia de texto no caminho do símbolo. Cada vez que o depurador precisa carregar símbolos para um módulo carregado recentemente, ele chama o servidor de símbolos para localizar os arquivos de símbolo apropriados. O servidor de símbolos localiza os arquivos em um *repositório de símbolos*. Essa é uma coleção de arquivos de símbolos, um índice e uma ferramenta que podem ser usados por um administrador para adicionar e excluir arquivos. Os arquivos são indexados de acordo com parâmetros exclusivos, como o carimbo de data/hora e o tamanho da imagem. As ferramentas de depuração para Windows contêm uma ferramenta de armazenamento de símbolos chamada SymStore.

Para obter mais informações, consulte:

-   [Usando SymSrv](using-symsrv.md)
-   [Usando SymStore](using-symstore.md)
-   [Usando outros armazenamentos de símbolo](using-other-symbol-stores.md)
-   [Opções de Command-Line de SymStore](symstore-command-line-options.md)
-   [Servidores de símbolos e firewalls da Internet](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos de Símbolo](symbol-files.md)
</dt> </dl>

 

 



