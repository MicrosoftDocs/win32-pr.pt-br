---
description: Há suporte para as seguintes formas de sintaxe para transações SymStore. O primeiro parâmetro deve sempre ser Add ou del. A ordem dos outros parâmetros não importa.
ms.assetid: d6d10adb-cb17-4ce3-b0e5-493b313ebdba
title: Opções de Command-Line de SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b69cdca9ee74cf01041375f26b2e151dc3ec5d
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298038"
---
# <a name="symstore-command-line-options"></a>Opções de Command-Line de SymStore

Há suporte para as seguintes formas de sintaxe para transações SymStore. O primeiro parâmetro deve sempre ser Add ou del. A ordem dos outros parâmetros não importa.

**SymStore adicionar** \[ **/l** **/o** **/p** **/r** **/compress** \] \[ **-: msg** *mensagem* \] \[ **-: rel** \] \[ **-: norefs** \] **/f** *arquivo* **/s** *Store* **/t** *produto* \[ **/v** *versão* \] \[ **/c** *Comentário* \] \[ **/d**  arquivo de log\]

**SymStore adicionar** \[ **/a** **/l** **/o** **/p** **/r** \] \[ **-: rel** \] \[ **-: norefs** \] **/g** *compartilhamento* **/f** *arquivo* **/x** *indexfile* \[ **/d** *logfile*\]

**SymStore adicionar** \[ **/o** **/compress** \] \[ **/p** \[ **-: msg** \| *mensagem* \] \[ **-: rel** \] \[ **-: norefs** \] \] **/y** *indexfile* **/g** *compartilhamento* **/s** *Store* **/t** *produto* \[ **/v** *versão* \] \[ **/c** *Comentário* \] \[ **/d**  arquivo de log\]

**consulta SymStore** \[ **/o** **/r** \] **/f** *arquivo* **/s** *Store* \[ **/d** *logfile*\]

**SymStore del** **/i** *ID* **/s** *Store* \[ **/o** \] \[ **/d** *logfile*\]

**SymStore** **/?**



| Parâmetro      | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /a             | Faz com que o SymStore acrescente novas informações de indexação a um arquivo de índice existente. (Essa opção só é usada com a opção/x.)                                                                                                                                                                                                                                                                                 |
| /c *Comentário*   | Especifica um comentário para a transação.                                                                                                                                                                                                                                                                                                                                                                     |
| /compress      | Faz com que o SymStore crie uma versão compactada de cada arquivo copiado para o repositório de símbolos em vez de usar uma cópia descompactada do arquivo. Essa opção só é válida ao armazenar arquivos e não ponteiros e não pode ser usada com a opção/p.                                                                                                                                                              |
| /d arquivo de *log*   | Especifica um arquivo de log a ser usado para a saída do comando. Se isso não for incluído, as informações da transação e outras saídas serão enviadas para stdout.                                                                                                                                                                                                                                                                     |
| /f *arquivo*      | Especifica um ou mais caminhos de arquivo (ou diretórios) a serem adicionados. Se um caminho de arquivo especificado começar com um símbolo ' @ ', será esperado um [arquivo de resposta](../midl/response-files.md) contendo uma lista de arquivos a serem adicionados (um caminho de arquivo por linha).                                                                                                                                             |
| /g *compartilhamento*     | Especifica o servidor e o compartilhamento onde os arquivos de símbolo foram armazenados originalmente. Quando usado com/f, o *compartilhamento* deve ser idêntico ao início do especificador de *arquivo* . Quando usado com/y, o *compartilhamento* deve ser o local dos arquivos de símbolo originais (não o arquivo de índice). Isso permite que você altere posteriormente essa parte do caminho do arquivo caso mova os arquivos de símbolo para um servidor e compartilhamento diferentes. |
| /i *ID*        | Especifica a cadeia de caracteres da ID da transação.                                                                                                                                                                                                                                                                                                                                                                         |
| /l             | Permite que o arquivo esteja em um diretório local em vez de um caminho de rede. (Essa opção só é usada com a opção/p.)                                                                                                                                                                                                                                                                                        |
| /o             | Faz com que o SymStore exiba a saída detalhada.                                                                                                                                                                                                                                                                                                                                                                   |
| /p             | Faz com que o SymStore armazene um ponteiro para o arquivo, em vez do próprio arquivo.                                                                                                                                                                                                                                                                                                                                 |
| /r             | Faz com que o SymStore adicione arquivos ou diretórios recursivamente.                                                                                                                                                                                                                                                                                                                                                     |
| /s *armazenar*     | Especifica o diretório raiz para o armazenamento de símbolo.                                                                                                                                                                                                                                                                                                                                                           |
| /t *produto*   | Especifica o nome do produto.                                                                                                                                                                                                                                                                                                                                                                           |
| /v *versão*   | Especifica a versão do produto.                                                                                                                                                                                                                                                                                                                                                                        |
| /x *indexfile* | Faz com que o SymStore não armazene os arquivos de símbolo reais. Em vez disso, o SymStore registra as informações no *indexfile* que permitirá que o symstore acesse os arquivos de símbolo posteriormente.                                                                                                                                                                                                                         |
| /y *indexfile* | Faz com que o SymStore Leia os dados de um arquivo criado com/x.                                                                                                                                                                                                                                                                                                                                                |
| -: Mensagem MSG  | Adiciona a mensagem especificada a cada arquivo. (Essa opção só pode ser usada quando/p é usado.)                                                                                                                                                                                                                                                                                                                     |
| -: REL          | Permite que os caminhos nos ponteiros de arquivo sejam relativos. Essa opção implica a opção/l. (Essa opção só pode ser usada quando/p é usado.)                                                                                                                                                                                                                                                                     |
| -: Norefs       | Omite a criação de arquivos de ponteiro de referência para os arquivos e os ponteiros que estão sendo armazenados. Essa opção só será válida durante a criação inicial de um armazenamento de símbolo se o armazenamento que está sendo alterado tiver sido criado com essa opção.                                                                                                                                                                                      |
| /?             | Exibe o texto de ajuda para o comando SymStore.                                                                                                                                                                                                                                                                                                                                                                 |



 

 

 



