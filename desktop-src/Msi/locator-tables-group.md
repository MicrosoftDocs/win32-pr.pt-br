---
description: O grupo tabelas do localizador é usado para localizar arquivos e aplicativos.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Grupo de tabelas do localizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629163"
---
# <a name="locator-tables-group"></a>Grupo de tabelas do localizador

O grupo tabelas do localizador é usado para localizar arquivos e aplicativos. Para procurar um arquivo, primeiro determine a assinatura do arquivo e, em seguida, localize o arquivo. As tabelas do localizador são usadas para pesquisar o registro, os dados de configuração do instalador, a árvore de diretórios ou os arquivos de .ini para a assinatura exclusiva de um arquivo. A assinatura de arquivo pode então ser verificada na [tabela de assinatura](signature-table.md) para verificar se um arquivo específico é realmente o arquivo que está sendo procurado e não outro arquivo com o mesmo nome. Se um registro em uma tabela do localizador não contiver uma chave na tabela de assinatura, o registro se referirá a um diretório e não a um arquivo.

O componente que controla um arquivo é encontrado na [tabela de arquivos](file-table.md) por meio da chave externa para a [tabela de componentes](component-table.md). O instalador resolve o local de um arquivo por meio da tabela de componentes porque cada arquivo pertence a um componente. O local de um componente é encontrado por meio de uma chave externa na tabela de componentes para a [tabela de diretórios](directory-table.md).

O local de um aplicativo é encontrado pesquisando os arquivos que compõem o aplicativo. O instalador também fornece duas tabelas para pesquisar versões anteriores de um aplicativo: a [tabela AppSearch](appsearch-table.md) e a [tabela CCPSearch](ccpsearch-table.md).

As tabelas a seguir compõem o grupo de tabelas do localizador e são usadas para determinar a assinatura do arquivo.

-   A [tabela RegLocator](reglocator-table.md) contém as informações necessárias para pesquisar um arquivo ou diretório no registro.
-   A [tabela IniLocator](inilocator-table.md) contém as informações necessárias para pesquisar um arquivo de .ini. o arquivo de .ini deve estar presente no diretório padrão do Microsoft Windows.
-   A [tabela CompLocator](complocator-table.md) contém as informações necessárias para pesquisar um arquivo ou um diretório usando os dados de configuração do instalador.
-   A [tabela DrLocator](drlocator-table.md) contém as informações necessárias para pesquisar um arquivo ou diretório na árvore de diretórios.
-   A [tabela AppSearch](appsearch-table.md) contém as propriedades que devem ser definidas para o resultado da pesquisa de uma assinatura de arquivo correspondente.
-   A [tabela CCPSearch](ccpsearch-table.md) contém a lista de assinaturas de arquivo, pelo menos uma delas precisa estar presente no computador de um usuário para o CCP (programa de verificação de conformidade).

 

 



