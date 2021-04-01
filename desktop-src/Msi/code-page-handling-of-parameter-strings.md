---
description: Você pode adicionar informações de localização a um banco de dados de instalação usando um editor de tabela de banco de dados, como o orca, fornecido com o SDK do Windows Installer ou chamando as funções de banco de dados de um aplicativo.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Manipulação de página de código de cadeias de caracteres de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164740"
---
# <a name="code-page-handling-of-parameter-strings"></a>Manipulação de página de código de cadeias de caracteres de parâmetro

Você pode adicionar informações de localização a um banco de dados de instalação usando um editor de tabela de banco de dados, como o orca, fornecido com o SDK do Windows Installer ou chamando as [funções de banco de dados](database-functions.md) de um aplicativo. Tenha cuidado para passar apenas parâmetros de cadeia de caracteres que usam a página de código do banco de dados que está sendo localizado. Se um parâmetro de cadeia de caracteres contiver caracteres que não podem ser representados pela página de código do banco de dados, o instalador retornará um erro ao chamar [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Para obter uma lista de páginas de código numérico, consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md).

Para obter mais informações, consulte [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md).

## <a name="adding-localization-information-to-a-database"></a>Adicionando informações de localização a um banco de dados

Quando você adiciona informações de localização a um banco de dados, a página de código do banco de dados deve ser suportada pelo sistema operacional. Não precisa ser a página de código atual do sistema. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) deve retornar **true** para a página de código do banco de dados. Como o sistema converte cadeias de caracteres ANSI em Unicode, haverá um erro se a página de código do usuário atual não for a mesma que a página de código do banco de dados.

Chamar a versão ANSI da API de Windows Installer converte a cadeia de caracteres localizada em Unicode usando a página de código do sistema atual. Quando o banco de dados é confirmado, a cadeia de caracteres Unicode é convertida em ANSI usando a página de código do banco de dados. Se a página de código do sistema atual for diferente da página de código da cadeia de caracteres localizada, o resultado poderá ser uma perda de dados e conversão de cadeia de caracteres incorreta.

O procedimento a seguir mostra como armazenar os dados de localização.

**Para armazenar dados de localização**

1.  Defina a página de código do banco de dados para a página de código da cadeia de caracteres localizada.
2.  Converta a cadeia de caracteres ANSI em Unicode usando a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e especifique a página de código dos dados localizados.
3.  Chame a versão Unicode da API de Windows Installer usando a cadeia de caracteres Unicode para adicionar os dados localizados.
4.  Confirme as alterações de localização no banco de dados usando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Você também pode adicionar informações de localização a um banco de dados de instalação importando e exportando arquivos mortos de texto ASCII. Para obter mais informações, consulte [manipulação de página de código de tabelas importadas e](code-page-handling-of-imported-and-exported-tables.md)exportadas.

 

 
