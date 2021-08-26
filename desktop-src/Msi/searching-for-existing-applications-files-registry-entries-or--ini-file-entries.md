---
description: Windows O instalador pode pesquisar um arquivo ou diretório específico durante uma instalação. Pesquisas de arquivo ou diretório são usadas para determinar se um usuário já instalou uma versão de um aplicativo.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Pesquisando aplicativos, arquivos, entradas do Registro ou .ini de arquivo existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9cf4b39f8a46ccd16e83c96ee6ca808b3a1bee32094da480d0226d8bdf283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041046"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Pesquisando aplicativos, arquivos, entradas do Registro ou .ini de arquivo existentes

Windows O instalador pode pesquisar um arquivo ou diretório específico durante uma instalação. Pesquisas de arquivo ou diretório são usadas para determinar se um usuário já instalou uma versão de um aplicativo.

[A Ação do AppSearch](appsearch-action.md) pesquisa em um sistema de usuários assinaturas de arquivo especificadas na [Tabela appSearch](appsearch-table.md). Se a ação AppSearch encontrar um arquivo ou diretório instalado com a assinatura especificada, ela define uma propriedade correspondente, também especificada na Tabela appSearch, para o local do arquivo ou diretório. Ao pesquisar um arquivo, a assinatura de arquivo também deve ser listada na [Tabela de Assinatura](signature-table.md). Se uma assinatura de arquivo estiver listada na Tabela AppSearch e não estiver listada na Tabela de Assinatura, a pesquisa procurará um diretório, uma entrada do Registro ou uma .ini de arquivo.

Para agilizar a pesquisa de um computador de usuário, o Instalador consulta as seguintes tabelas de banco de dados de localizador na ordem listada para um local de pesquisa sugerido:

-   Se a assinatura de arquivo estiver listada na [Tabela compLocator](complocator-table.md), o local de pesquisa sugerido será o caminho da chave de um componente. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o Instalador consultará a Tabela [RegLocator](reglocator-table.md) para um local sugerido.
-   Se a assinatura de arquivo estiver listada na [Tabela RegLocator](reglocator-table.md), o local de pesquisa sugerido será um caminho de chave gravado no registro de usuário. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o Instalador consultará a tabela [IniLocator](inilocator-table.md) para um local sugerido.
-   Se a assinatura de arquivo estiver listada na Tabela [IniLocator](inilocator-table.md), o local de pesquisa sugerido será um caminho de chave escrito em um arquivo .ini presente no diretório padrão Windows de um sistema de usuário. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o Instalador consultará a Tabela [DrLocator](drlocator-table.md) para um local sugerido.
-   Se a assinatura de arquivo estiver listada na [Tabela DrLocator](drlocator-table.md), o local de pesquisa sugerido será um caminho na árvore de diretórios do usuário. A profundidade dos níveis de subdiretório a ser pesquisado abaixo desse local também é especificada nesta tabela.

Na primeira vez que o Instalador localiza a assinatura do arquivo em um local sugerido, ele para de pesquisar esse arquivo ou diretório e define a propriedade correspondente na [Tabela appSearch](appsearch-table.md). Para saber mais, consulte o seguinte:

-   [Pesquisando todas as unidades fixas para um arquivo](searching-all-fixed-drives-for-a-file.md)
-   [Pesquisando um diretório e um arquivo no diretório](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Pesquisando um arquivo e criando uma propriedade que mantém o caminho do arquivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Procurando um arquivo em um local específico](searching-for-a-file-in-a-specific-location.md)
-   [Pesquisando uma entrada do Registro e criando uma propriedade que mantém o valor do Registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



