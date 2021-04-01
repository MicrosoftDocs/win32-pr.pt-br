---
description: O Windows Installer armazena todas as cadeias de caracteres de banco de dados em um único pool de cadeias compartilhada para reduzir o tamanho do banco de dados e melhorar o desempenho.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Validação de String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090935"
---
# <a name="string-pool-validation"></a>Validação de String-Pool

O Windows Installer armazena todas as cadeias de caracteres de banco de dados em um único pool de cadeias compartilhada para reduzir o tamanho do banco de dados e melhorar o desempenho. O único meio de validar o pool de cadeias de caracteres é usar a ferramenta MsiInfo encontrada no SDK do Windows Installer.

A verificação do pool de cadeias de caracteres consiste em duas verificações principais:

-   [Testes de cadeia de caracteres DBCS](#dbcs-string-tests)
-   [Verificação de contagem de referência](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Testes de cadeia de caracteres DBCS

Os testes de cadeia de caracteres DBCS examinam cada cadeia de caracteres no banco de dados em busca de dois critérios: para pacotes com uma página de código neutra marcada, se qualquer caractere for um caractere estendido (maior que 127), a cadeia de caracteres será sinalizada e uma mensagem será exibida informando que a página de código do banco de dados é inválida, pois esses caracteres exigem uma

Se o banco de dados tiver uma página de código, cada cadeia de caracteres será verificada em busca de um indicador DBCS inválido. Se uma cadeia de caracteres não neutra tiver sido marcada incorretamente, os caracteres não serão renderizados corretamente. (Isso é mais comumente causado pela força da página de código a um valor específico usando o \_ Tabela ForceCodepage com cadeias de caracteres não neutras já existentes no banco de dados.) Observe que essa verificação requer que a página de código do banco de dados seja instalada no sistema.

Se houver um problema de página de código, o usuário poderá corrigir o erro usando a \_ tabela ForceCodepage para forçar a página de código do banco de dados para o valor apropriado. Para obter mais informações, consulte [manipulação de página de código](code-page-handling-windows-installer-.md).

## <a name="reference-count-verification"></a>Verificação de contagem de referência

Para verificar as contagens de referência de todas as cadeias de caracteres, todas as tabelas são verificadas em busca de valores de cadeia, uma contagem de cada cadeia de caracteres distinta é mantida e o resultado é comparado à contagem de referência armazenada no pool de cadeias de caracteres de banco de dados.

Se houver um problema de contagem de referência de cadeia de caracteres, o usuário deverá exportar imediatamente cada tabela do banco de dados usando [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), criar um novo banco de dados e importar as tabelas para o novo banco de dados usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). O novo banco de dados tem o mesmo conteúdo do banco de dados antigo, mas as contagens de referência de cadeia de caracteres estão corretas. A adição ou exclusão de dados de um banco de dado com um pool de cadeias de caracteres corrompidos pode aumentar a corrupção do banco de dados e a perda de dado. portanto, é importante executar essas etapas rapidamente para evitar mais perda de dados.

Ao recriar bancos de dados, lembre-se de inserir todos os armazenamentos e fluxos necessários no novo banco de dados (consulte tabela de [ \_ fluxos](-streams-table.md) e tabela de [ \_ armazenamentos](-storages-table.md)) e lembre-se de problemas de página de código. Lembre-se também de definir cada uma das propriedades de [fluxo de informações de resumo](summary-information-stream.md) necessárias.

 

 



