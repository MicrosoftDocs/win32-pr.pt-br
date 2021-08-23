---
description: Sempre de definir a página de código de um banco de dados antes de adicionar informações de localização.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Definindo a página de código de um banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c9ac1840b624b821dff6a85bee94607cd9568dcd6bb9b01025cb02f87c5c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628536"
---
# <a name="setting-the-code-page-of-a-database"></a>Definindo a página de código de um banco de dados

Sempre de definir a página de código de um banco de dados antes de adicionar informações de localização. Não é recomendável tentar definir a página de código depois de inserir dados no banco de dados porque isso pode corromper caracteres estendidos. A localização pode ser muito facilitada começando com um banco de dados que é neutro na página de código. Para obter detalhes, consulte [Criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md). Você pode determinar a página de código atual de um banco de dados, conforme descrito em [Determinando a página](determining-an-installation-database-s-code-page.md)de código de um banco de dados de instalação . Consulte [Localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para ver uma lista de páginas de código numérico.

Você pode definir a página de código de um banco de dados em branco ou um banco de dados com uma página de código neutra importando um arquivo de arquivo de texto com uma página de código não neutra com [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Isso define a página de código do banco de dados para a página de código do arquivo importado. Todos os arquivos de arquivo subsequentemente importados para o banco de dados devem ter a mesma página de código que o primeiro arquivo. Se um arquivo de arquivo de texto for exportado de um banco de dados, a página de código do arquivo morto será a mesma do banco de dados pai. Consulte [Tratamento de página de código de tabelas importadas e exportadas.](code-page-handling-of-imported-and-exported-tables.md)

A página de código de qualquer banco de dados pode ser definida como uma página de código numérico especificada usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) para importar um arquivo de arquivo de texto com o seguinte formato: duas linhas em branco; seguido por uma linha que contém a página de código numérico, um separador de tabulação e a cadeia de caracteres exata: \_ ForceCodepage. Observe que, com Windows 2000, isso converte todas as cadeias de caracteres no banco de dados para a página de código \_ de ForceCodepage. Isso pode ser destinado ao localizar um banco de dados existente e traduzir todas as cadeias de caracteres não neutras para a nova página de código. No entanto, isso causará um erro se o banco de dados contiver cadeias de caracteres não neutras que não devem ser traduzidas.

O utilitário WiLangId.vbs fornece um exemplo de como definir a página de código de um pacote usando o [**método Import**](database-import.md). Uma cópia de WiLangId.vbs é fornecida no SDK Windows Installer. Você pode usar esse utilitário para determinar as versões de idioma com suporte pelo banco de dados (Pacote), o idioma que o instalador usa para quaisquer cadeias de caracteres na interface do usuário que não são autoradas no banco de dados (Produto) ou na única página de código ANSI para o pool de cadeias de caracteres (Codepage). Para obter informações sobre como usar WiLangId.vbs consulte a página de ajuda: [Gerenciar idioma e página de código.](manage-language-and-codepage.md)

Para determinar os valores de Product, Package e Codepage, execute WiLangId.vbs da seguinte forma.

**cscript wilangid.vbs** *\[ caminho para \] o banco de dados*

Para definir a página de código do pacote, execute a linha de comando a seguir.

**cscript wilangid.vbs** *\[ caminho para \] o valor codepage do banco* **de** *\[ dados \]*

Por exemplo, para definir a página de código test.msi para o valor numérico da página de código ANSI 1252, execute a linha de comando a seguir.

**cscript wilangid.vbs c: \\ temp \\test.msi Codepage 1252**

 

 



