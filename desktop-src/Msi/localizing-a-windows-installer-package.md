---
description: Para obter informações gerais sobre a localização, consulte serviços de globalização.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Localizando um pacote de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090637"
---
# <a name="localizing-a-windows-installer-package"></a>Localizando um pacote de Windows Installer

Para obter informações gerais sobre a localização, consulte [serviços de globalização](../intl/globalization-services.md). Localizar um pacote de Windows Installer requer a modificação das cadeias de caracteres exibidas pela interface do usuário e também pode exigir a adição ou modificação de recursos do produto. Por exemplo, a localização pode incluir a adição de DLLs internacionais e arquivos localizados ao produto.

**Para localizar um pacote de Windows Installer**

1.  Prepare-se para a localização ao criar o pacote de instalação original. Projete o layout de arquivos localizados de forma que diferentes versões de idioma possam coexistir com segurança quando instalado no computador do usuário. Organize arquivos que exigem localização em componentes separados e instale esses arquivos em diretórios separados. Crie um banco de dados de instalação base que tenha uma página de controle neutra. Consulte [preparando um pacote de Windows Installer para localização](preparing-a-windows-installer-package-for-localization.md).
2.  Sempre defina a página de código do banco de dados que está sendo localizado antes de adicionar dados localizados. Se a página de código do banco de dados que está sendo localizado for neutra, consulte [definindo a página de código de um banco de dados](setting-the-code-page-of-a-database.md). Para determinar a página de código, consulte [determinando a página de código de um banco de dados de instalação](determining-an-installation-database-s-code-page.md).
3.  Importe uma [tabela de erro](error-table.md) localizada e uma [tabela ActionText](actiontext-table.md) para o banco de dados. Para obter mais informações, consulte [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) para obter uma lista de idiomas com suporte no Microsoft Windows Software Development Kit (SDK). Você pode importar essas tabelas usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).
4.  Modifique qualquer uma das outras colunas localizáveis no banco de dados usando um editor de tabela ou consultas SQL. Para as funções de acesso do SQL, consulte [trabalhando com consultas](working-with-queries.md). Os tópicos das tabelas de banco de dados identificam quais colunas de banco de dados podem ser localizadas. Para obter mais informações, consulte a lista de tabelas em [tabelas de banco de dados](database-tables.md).
5.  Defina a propriedade [**ProductLanguage**](productlanguage.md) na [tabela de propriedades](property-table.md) como o LANGID do banco de dados. Ao criar um pacote como idioma neutro, defina a propriedade ProductLanguage como 0 e use a fonte MS Shell Dlg como o estilo de texto para todas as caixas de diálogo criadas. Como algumas fontes não dão suporte a todos os conjuntos de caracteres, você pode garantir que o texto seja exibido corretamente em todas as versões localizadas do sistema operacional usando essa fonte.
6.  Defina o campo idioma da propriedade [**Resumo do modelo**](template-summary.md) para refletir o LANGID do banco de dados.
7.  Se as cadeias de caracteres de texto no [fluxo de informações de resumo](summary-information-stream.md) forem localizadas, defina a propriedade de [**Resumo CodePage**](codepage-summary.md) como a página de código.
8.  Defina a propriedade [**ProductCode**](productcode.md) na [tabela de propriedades](property-table.md) e defina o código do pacote na propriedade Resumo do número de [**revisão**](revision-number-summary.md) como um novo código de pacote. Um produto localizado é considerado um produto diferente. Por exemplo, as versões em alemão e em inglês de um aplicativo são consideradas dois produtos diferentes e devem ter códigos de produto diferentes.
9.  A localização pode exigir a modificação de recursos que já existem ou a adição de novos recursos, como arquivos ou chaves do registro. Verifique se o código do componente foi alterado para cada componente existente que tenha um novo recurso adicionado. Outras modificações também podem exigir alterações no código de um componente. Para obter mais informações, consulte [alterando o código do componente](changing-the-component-code.md).
10. Certifique-se de salvar a localização e outras alterações no banco de dados salvando o pacote com a ferramenta de edição ou chamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Para obter mais informações, consulte [um exemplo de localização](a-localization-example.md).

 

 
