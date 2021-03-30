---
description: Sempre defina a página de código de um banco de dados antes de adicionar qualquer informação de localização.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Configurando a página de código de um banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647526"
---
# <a name="setting-the-code-page-of-a-database"></a>Configurando a página de código de um banco de dados

Sempre defina a página de código de um banco de dados antes de adicionar qualquer informação de localização. Não é recomendável tentar definir a página de código depois de inserir dados no banco de dado, pois isso pode corromper os caracteres estendidos. A localização pode ser bastante facilitada com o início de um banco de dados que é uma página de código neutra. Para obter detalhes, consulte [criando um banco de dados com uma página de código neutra](creating-a-database-with-a-neutral-code-page.md). Você pode determinar a página de código atual de um banco de dados conforme descrito em [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md). Consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para obter uma lista de páginas de código numérico.

Você pode definir a página de código de um banco de dados em branco ou um banco de dados com uma página de código neutra, importando um arquivo morto de texto que tenha uma página de código não neutra com [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Isso define a página de código do banco de dados para a página de código do arquivo importado. Todos os arquivos mortos subsequentemente importados para o banco de dados devem ter a mesma página de código que o primeiro arquivo. Se um arquivo morto de texto for exportado de um banco de dados, a página de código do arquivo morto será a mesma do banco de dados pai. Consulte [manipulação de página de código de tabelas importadas e](code-page-handling-of-imported-and-exported-tables.md)exportadas.

A página de código de qualquer banco de dados pode ser definida como uma página de código numérico especificada usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) para importar um arquivo morto de texto com o seguinte formato: duas linhas em branco; seguido por uma linha que contém a página de código numérico, um delimitador de tabulação e a cadeia de caracteres exata: \_ ForceCodepage. Observe que, com o Windows 2000, isso traduz todas as cadeias de caracteres no banco de dados para a página de código do \_ ForceCodepage. Isso pode ser destinado ao localizar um banco de dados existente e traduzir todas as cadeias de caracteres não neutras para a nova página de código. No entanto, isso causará um erro se o banco de dados contiver cadeias de caracteres não neutras que não devem ser traduzidas.

O utilitário WiLangId.vbs fornece um exemplo de como definir a página de código de um pacote usando o [**método de importação**](database-import.md). Uma cópia de WiLangId.vbs é fornecida no SDK do Windows Installer. Você pode usar esse utilitário para determinar as versões de idioma com suporte do banco de dados (pacote), o idioma usado pelo instalador para qualquer cadeia de caracteres na interface do usuário que não é criada no banco de dados (produto) ou a página de código ANSI única para o pool de cadeias de caracteres (CodePage). Para obter informações sobre como usar WiLangId.vbs consulte a página de ajuda: [gerenciar idioma e página de código](manage-language-and-codepage.md).

Para determinar os valores do produto, pacote e página de código, execute WiLangId.vbs da seguinte maneira.

**cscript wilangid.vbs** *\[ caminho para o \] banco de dados*

Para definir a página de código do pacote, execute a seguinte linha de comando.

**cscript wilangid.vbs** caminho para o *\[ valor \]* **CodePage** do *\[ banco de dados \]*

Por exemplo, para definir a página de código de test.msi como o valor numérico de páginas de códigos ANSI 1252, execute a linha de comando a seguir.

**cscript wilangid.vbs c: \\ temp \\test.msi página de código 1252**

 

 



