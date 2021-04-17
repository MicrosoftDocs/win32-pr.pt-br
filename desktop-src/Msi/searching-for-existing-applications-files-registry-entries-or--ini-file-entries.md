---
description: Windows Installer pode procurar um arquivo ou diretório específico durante uma instalação. Pesquisas de arquivo ou diretório são usadas para determinar se um usuário já instalou uma versão de um aplicativo.
ms.assetid: a78ca652-c730-4231-80f2-60cf0bad5b02
title: Pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41d0ebf8943d1fb82b7c0901a62230e6befdcba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769308"
---
# <a name="searching-for-existing-applications-files-registry-entries-or-ini-file-entries"></a>Pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes

Windows Installer pode procurar um arquivo ou diretório específico durante uma instalação. Pesquisas de arquivo ou diretório são usadas para determinar se um usuário já instalou uma versão de um aplicativo.

A [ação AppSearch](appsearch-action.md) pesquisa um sistema de usuário em busca de assinaturas de arquivo que são especificadas na [tabela AppSearch](appsearch-table.md). Se a ação AppSearch encontrar um arquivo ou diretório instalado com a assinatura especificada, ele definirá uma propriedade correspondente, também especificada na tabela AppSearch, para o local do arquivo ou diretório. Ao pesquisar um arquivo, a assinatura de arquivo também deve ser listada na [tabela de assinatura](signature-table.md). Se uma assinatura de arquivo estiver listada na tabela AppSearch e não estiver listada na tabela de assinatura, a pesquisa procurará um diretório, uma entrada de registro ou uma entrada de arquivo. ini.

Para agilizar a pesquisa de um computador de usuário, o instalador consulta as seguintes tabelas de banco de dados do localizador na ordem listada para um local de pesquisa sugerido:

-   Se a assinatura de arquivo estiver listada na [tabela CompLocator](complocator-table.md), o local de pesquisa sugerido será o caminho de chave de um componente. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o instalador consultará a [tabela RegLocator](reglocator-table.md) em busca de um local sugerido.
-   Se a assinatura de arquivo estiver listada na [tabela RegLocator](reglocator-table.md), o local de pesquisa sugerido será um caminho de chave escrito no registro do usuário. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o instalador consultará a [tabela IniLocator](inilocator-table.md) em busca de um local sugerido.
-   Se a assinatura de arquivo estiver listada na [tabela IniLocator](inilocator-table.md), o local de pesquisa sugerido será um caminho de chave escrito em um arquivo. ini presente no diretório padrão do Windows de um sistema de usuário. Se a assinatura não estiver listada nesta tabela ou não estiver instalada no local sugerido, o instalador consultará a [tabela DrLocator](drlocator-table.md) em busca de um local sugerido.
-   Se a assinatura do arquivo estiver listada na [tabela DrLocator](drlocator-table.md), o local de pesquisa sugerido será um caminho na árvore de diretórios do usuário. A profundidade dos níveis de subdiretórios a serem pesquisados abaixo desse local também é especificada nesta tabela.

Na primeira vez que o instalador encontrar a assinatura de arquivo em um local sugerido, ele interromperá a pesquisa desse arquivo ou diretório e definirá a propriedade correspondente na [tabela AppSearch](appsearch-table.md). Para saber mais, consulte o seguinte:

-   [Pesquisando todas as unidades fixas de um arquivo](searching-all-fixed-drives-for-a-file.md)
-   [Procurando um diretório e um arquivo no diretório](searching-for-a-directory-and-a-file-in-the-directory.md)
-   [Procurando um arquivo e criando uma propriedade que contém o caminho do arquivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
-   [Procurando um arquivo em um local específico](searching-for-a-file-in-a-specific-location.md)
-   [Procurando uma entrada de registro e criando uma propriedade que contém o valor do registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)

 

 



