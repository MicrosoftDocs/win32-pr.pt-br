---
description: Msidb.exe usa MsiDatabaseImport e MsiDatabaseExport para importar e exportar tabelas e fluxos de banco de dados.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756899"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para importar e exportar [tabelas](database-tables.md) e fluxos de banco de dados.

Se o modo, a pasta, o banco de dados e a lista de tabelas forem especificados na linha de comando, Msidb.exe não abrirá nenhuma interface do usuário e funcionará como um utilitário de linha de comando silencioso adequado para o script de compilação.

## <a name="syntax"></a>Syntax

**MsiDb** *{opção} ***...** _{opção}_* _..._ * * {tabela} ***...** _{tabela}_

## <a name="command-line-options"></a>Opções de linha de comando

Msidb.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço.



| Opção | Descrição                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importe arquivos mortos de texto da pasta para o banco de dados. Os nomes de tabela para importação são nomes de arquivo com 8 caracteres de comprimento com uma extensão ". IDT". Nomes mais longos são truncados para 8 caracteres, se fornecidos pelo comando para importação. Especificações de curinga padrão podem ser usadas.                                                                 |
| -E     | Exportar tabelas selecionadas do banco de dados para arquivos de texto arquivados na pasta. Os nomes de tabela para exportação são nomes de tabela. Somente a especificação curinga, " \* ", pode ser usada. As tabelas podem ser exportadas de um banco de dados somente leitura.                                                                                                               |
| -c     | Cria um novo arquivo de banco de dados e importa tabelas. Substitui um arquivo de banco de dados existente.                                                                                                                                                                                                                                               |
| -f     | Especifica a pasta que contém os arquivos mortos de texto para tabelas e fluxos. Se a pasta que contém os arquivos mortos de texto não for especificada, o utilitário solicitará ao usuário a pasta.                                                                                                                                       |
| -d     | Caminho totalmente qualificado para o arquivo de banco de dados.                                                                                                                                                                                                                                                                                          |
| -M     | Caminho totalmente qualificado para o banco de dados que deve ser mesclado no. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10. Se o banco de dados não for especificado na linha de comando, o utilitário solicitará ao usuário o banco de dados.                                       |
| -T     | Caminho totalmente qualificado para a transformação a ser aplicada. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                     |
| -j     | Nome do armazenamento a ser removido do banco de dados. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                             |
| -k     | Nome do fluxo a ser removido do banco de dados. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                                 |
| -X     | Nome do fluxo para salvar em um arquivo de disco no diretório atual. Essa opção está disponível somente no modo de linha de comando silencioso. Os fluxos de dados binários são armazenados como arquivos separados com a extensão ". IBD". O nome de arquivo binário usado são dados de chave primária para a linha que contém o fluxo.                                                  |
| -w     | Nome do armazenamento para salvar em um arquivo de disco no diretório atual. Essa opção está disponível somente no modo de linha de comando silencioso.                                                                                                                                                                                                         |
| -a     | Nome do arquivo a ser adicionado ao banco de dados como um fluxo. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10. Os fluxos de dados binários são armazenados como arquivos separados com a extensão ". IBD". O nome de arquivo binário usado são dados de chave primária para a linha que contém o fluxo. |
| -r     | Nome do armazenamento a ser adicionado ao banco de dados como um subarmazenamento. Essa opção está disponível somente no modo de linha de comando silencioso. Várias instâncias dessa opção podem ocorrer no máximo 10.                                                                                                                                                     |
| -S     | Truncar nomes de tabela para 8 caracteres na exportação para uma. IDT. O nome da tabela é truncado para 8 caracteres e a extensão ". IDT" é adicionada.                                                                                                                                                                                           |
| -?     | Exibe a caixa de diálogo de ajuda da linha de comando                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Ao usar nomes longos de filespaces com espaços, use aspas ao seu respeito. Por exemplo, para um banco de dados que está na pasta "meus documentos", especifique-o como "c: \\ My Documents".

 

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



