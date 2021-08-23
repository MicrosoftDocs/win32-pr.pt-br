---
description: Msidb.exe usa MsiDatabaseImport e MsiDatabaseExport para importar e exportar fluxos e tabelas de banco de dados.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bff646ae3e933be5dbe37a774b72c10a0183fe9c793305292c9a11c4f417be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012925"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para importar e [exportar](database-tables.md) fluxos e tabelas de banco de dados.

Se o modo, a pasta, o banco de dados e a lista de tabelas são especificados na linha de comando, o Msidb.exe não abrirá nenhuma interface do usuário e operará como um utilitário de linha de comando silencioso adequado para o script de build.

## <a name="syntax"></a>Syntax

**MsiDb** *{option}***...** _{option}_* _..._ * *{table}***...** _{table}_

## <a name="command-line-options"></a>Opções de linha de comando

Msidb.exe usa as seguintes opções de linha de comando sem valor de maiúsculas e minúsculas. Um delimiter de barra também pode ser usado no lugar de um traço.



| Opção | Descrição                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importe arquivos de arquivo de texto da pasta para o banco de dados. Os nomes de tabela para importação são nomes de arquivo de 8 caracteres com uma extensão ".idt". Nomes mais longos são truncados para 8 caracteres, se fornecidos pelo comando para importação. Especificações de curinga padrão podem ser usadas.                                                                 |
| -E     | Exporte tabelas selecionadas do banco de dados para arquivos de arquivo de texto na pasta . Os nomes de tabela para exportação são nomes de tabela. Somente a especificação de curinga, \* " ", pode ser usada. As tabelas podem ser exportadas de um banco de dados somente leitura.                                                                                                               |
| -c     | Cria um novo arquivo de banco de dados e importa tabelas. Substitui um arquivo de banco de dados existente.                                                                                                                                                                                                                                               |
| -f     | Especifica a pasta que contém os arquivos de arquivo de texto para tabelas e fluxos. Se a pasta que contém os arquivos de arquivo de texto não for especificada, o utilitário solicitará a pasta ao usuário.                                                                                                                                       |
| -d     | Caminho totalmente qualificado para o arquivo de banco de dados.                                                                                                                                                                                                                                                                                          |
| -M     | Caminho totalmente qualificado para o banco de dados que deve ser mesclado. Essa opção só está disponível no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10. Se o banco de dados não for especificado na linha de comando, o utilitário solicitará ao usuário o banco de dados.                                       |
| -T     | Caminho totalmente qualificado para a transformação a ser aplicada. Essa opção só está disponível no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                     |
| -j     | Nome do armazenamento a ser removido do banco de dados. Essa opção só está disponível no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                             |
| -k     | Nome do fluxo a ser removido do banco de dados. Essa opção está disponível somente no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                                 |
| -X     | Nome do fluxo a ser salvo em um arquivo de disco no diretório atual. Essa opção só está disponível no modo de linha de comando silenciosa. Os fluxos de dados binários são armazenados como arquivos separados com a extensão ".ibd". O nome de arquivo binário usado são dados de chave primária para a linha que contém o fluxo.                                                  |
| -w     | Nome do armazenamento a ser salvo em um arquivo de disco no diretório atual. Essa opção só está disponível no modo de linha de comando silenciosa.                                                                                                                                                                                                         |
| -a     | Nome do arquivo a ser adicionar ao banco de dados como um fluxo. Essa opção só está disponível no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10. Os fluxos de dados binários são armazenados como arquivos separados com a extensão ".ibd". O nome de arquivo binário usado são dados de chave primária para a linha que contém o fluxo. |
| -r     | Nome do armazenamento a ser adicionar ao banco de dados como um substorage. Essa opção está disponível somente no modo de linha de comando silenciosa. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                     |
| -S     | Truncar nomes de tabela para 8 caracteres na exportação para um .idt. O nome da tabela é truncado para 8 caracteres e a extensão ".idt" é adicionada.                                                                                                                                                                                           |
| -?     | Exibe a caixa de diálogo de ajuda da linha de comando                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Ao usar nomes de arquivo longos com espaços, use aspas ao redor deles. Por exemplo, para um banco de dados que está na pasta "Meus Documentos", especifique-o como "c: \\ meus documentos".

 

Essa ferramenta só está disponível nos componentes [do SDK Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



