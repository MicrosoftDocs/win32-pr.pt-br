---
title: Gerenciando arquivos e dados
description: os usuários têm acesso mais fácil a arquivos e dados no Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9091a2d9bb2cf01d4f9b514c55e78f2f989f01d6d64a929608e14c32bfd395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086649"
---
# <a name="managing-files-and-data"></a>Gerenciando arquivos e dados

os usuários têm acesso mais fácil a arquivos e dados no Windows 7. novas APIs tornam os arquivos e exibições mais informativos, permitindo que os aplicativos forneçam informações relevantes e impróprias para o Windows Explorer. Além disso, os aplicativos se beneficiam do novo modelo de *bibliotecas* , uma noção mais abstrata e útil do espaço de armazenamento do usuário que as pastas e também podem participar de bibliotecas comuns de tipos de arquivos semelhantes que são compartilhados por diferentes aplicativos.

## <a name="libraries"></a>Bibliotecas

o Windows 7 apresenta o conceito de *bibliotecas* como destinos em que os desenvolvedores e os usuários finais podem localizar e organizar seus dados como coleções de itens que podem abranger vários locais no computador local, bem como em computadores remotos.

As APIs de *biblioteca* fornecem uma maneira simples para os desenvolvedores criarem aplicativos que criam, interagem com e dão suporte a *bibliotecas* como itens de primeira classe em aplicativos. As *bibliotecas* também podem ser selecionadas usando a caixa de diálogo Seletor de pasta. Os aplicativos podem enumerar escopos de biblioteca relevantes ou podem usar a biblioteca diretamente como uma pasta. (consulte [bibliotecas de Windows](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) e [bibliotecas de Windows 7: recursos para desenvolvedores](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).

![biblioteca de imagens do Windows 7](images/windows7-10.jpg)

*Biblioteca de imagens* mostra suas imagens, independentemente de onde elas estão armazenadas

## <a name="file-formats-and-data-stores"></a>Formatos de arquivo e armazenamentos de dados

no Windows 7, o Windows Explorer facilita o gerenciamento e a manipulação de arquivos para o usuário de várias maneiras:

-   A visualização do tipo de arquivo de seu aplicativo é mais acessível com um novo botão que permite aos usuários mostrar e ocultar o painel de visualização.
-   As pilhas visuais de imersão agregam imagens em miniatura para tipos de arquivo em uma exibição.
-   Windows Os modos de exibição do Explorer mostram informações úteis com base nas propriedades gravadas com seu manipulador de propriedades.
-   Trechos de documento e realce de visita usam a implementação da interface do **IFilter** para facilitar a pesquisa e a localização de arquivos.
-   Os verbos e comandos do menu de contexto são mais fáceis do que nunca implementar.

Ao implementar todos os manipuladores de formato apropriados para os itens retornados do seu manipulador de protocolo, os resultados da pesquisa de seu armazenamento de dados personalizado podem ser tão ricos quanto os resultados da pesquisa de arquivos. As *bibliotecas* são criadas automaticamente para seus manipuladores de protocolo para que os usuários possam criar o escopo de suas pesquisas com facilidade. E a lógica para a criação de *bibliotecas* pode ser facilmente personalizada por meio do registro. (consulte [desenvolvendo filtros para Windows pesquisa](../search/-search-3x-wds-extidx-filters.md).)

![biblioteca de documentos do Windows 7](images/windows7-11.jpg)

no Windows 7, o Windows Explorer facilita o gerenciamento e a manipulação de arquivos

 

 