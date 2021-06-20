---
title: Estendendo o índice (recursos herdados do ambiente Windows)
description: Saiba como estender o índice no Windows Desktop Search 2. x. Para versões do Windows posteriores ao Windows XP e ao Windows Server 2003, use o Windows Search em vez disso.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407349"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a>Estendendo o índice (recursos herdados do ambiente Windows)

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

O uso do e do desenvolvimento para as versões 2. x do Microsoft Windows Desktop Search (WDS) é fortemente desencorajado em favor do [Windows Search](../search/-search-3x-wds-overview.md).

O WDS pode ser estendido para indexar o conteúdo de novos tipos de arquivo e armazenamentos de dados. Atualmente, o WDS 2. x contém filtros para mais de 200 tipos de itens (incluindo itens de texto sem formatação, como HTML, XML e arquivos de código-fonte) e usa o mesmo [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)e a mesma tecnologia de manipulador de protocolo que os serviços do SharePoint. Se você já tiver implementações de filtro instaladas para os novos tipos de arquivo, o WDS poderá usar as interfaces de filtro existentes para indexar esses dados.

Os suplementos do WDS 2. x permitem que o índice Percorra e analise novos dados e estruturas de dados para obter informações a serem adicionadas ao catálogo pesquisável. Esses suplementos também podem estender o Shell do Windows para associar ícones e manipuladores de menu de contexto aos novos tipos de arquivo e armazenamentos de dados. Para incluir novos tipos de arquivo no catálogo do WDS, um suplemento deve implementar a interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter). Para incluir novos armazenamentos de dados, um suplemento deve ser um manipulador de protocolo. Se o novo armazenamento de dados incluir arquivos incorporados ou novos tipos de arquivo, também será necessário escrever um filtro apropriado.

> [!Note]
>
> Filtros e manipuladores de protocolo devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que todos os suplementos são executados.

 

## <a name="adding-file-types-to-the-index"></a>Adicionando tipos de arquivo ao índice

Os suplementos podem estender o WDS para indexar tipos de arquivo novos ou proprietários e associar cada novo tipo de arquivo a um menu de contexto ou ícone específico de arquivo. Para fazer isso, você pode criar e registrar um suplemento que:

1.  Implementa uma interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para cada tipo de arquivo, de modo que o WDS possa acessar e indexar o texto e os metadados do tipo de arquivo.
2.  Implementa as interfaces **IExtractIcon** e **IContextMenu** para adicionar ícones e menus de contexto para maior integração e usabilidade.

Para obter uma discussão sobre a implementação de filtros, consulte [desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md).

## <a name="adding-data-stores-to-the-index"></a>Adicionando armazenamentos de dados ao índice

Os suplementos podem estender o WDS para indexar novos armazenamentos de dados e associar arquivos a um menu de contexto ou ícone específico de arquivo. Para fazer isso, você pode criar e registrar um manipulador de protocolo que:

1.  Implementa as interfaces **ISearchProtocol** e **IUrlAccessor** para processar e associar itens individuais na fonte de conteúdo. O WDS usa URLs para identificar itens de forma exclusiva, independentemente de esses itens estarem no sistema de arquivos, dentro de uma loja do tipo banco de dados ou na Web.
2.  Implementa a interface **IPersistFolder** e partes da interface **IShellFolder** para adicionar ícones e menus de contexto para maior integração e usabilidade.

Para obter uma discussão sobre a implementação de manipuladores de protocolo, consulte [desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md).

## <a name="add-in-installer-guidelines"></a>Diretrizes do instalador do suplemento

A instalação de um suplemento deve seguir as seguintes diretrizes:

-   O instalador deve usar o EXE ou o instalador MSI.
-   As notas de versão devem ser fornecidas.
-   Uma entrada **Adicionar/remover programas** deve ser criada para cada suplemento instalado.
-   O instalador deve assumir todas as configurações do registro para o tipo de arquivo específico ou o armazenamento que o suplemento atual compreende.
-   Se um suplemento anterior estiver sendo substituído, o instalador deverá notificar o usuário.
-   Se um suplemento mais recente tiver substituído o suplemento anterior, deverá haver a capacidade de restaurar a funcionalidade do suplemento anterior e torná-lo o suplemento padrão para esse tipo de arquivo ou armazenar novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Visio**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
