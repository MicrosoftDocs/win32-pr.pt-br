---
description: O registro de um tipo de arquivo é a primeira etapa na criação de uma associação de arquivo, que torna esse tipo de arquivo &\# 0034; conhecido&\# 0034; para o Shell. No entanto, sem manipuladores de tipo de arquivo, o shell não consegue expor informações ao usuário do e sobre o arquivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Manipuladores de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827013"
---
# <a name="file-type-handlers"></a>Manipuladores de tipo de arquivo

O [registro de um tipo de arquivo](fa-how-work.md) é a primeira etapa na criação de uma associação de arquivo, que torna esse tipo de arquivo "conhecido" para o Shell. No entanto, sem manipuladores de tipo de arquivo, o shell não consegue expor informações ao usuário do e sobre o arquivo.

Este tópico é organizado da seguinte maneira:

-   [Criar um tipo de arquivo conhecido pelo shell](#make-a-file-type-known-to-shell)
-   [Descrições do manipulador de tipo de arquivo](#file-type-handler-descriptions)
-   [Tópicos relacionados](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Criar um tipo de arquivo conhecido pelo shell

Na captura de tela a seguir do Windows Explorer, o arquivo de imagem deserto. conhecido aparece na biblioteca **imagens** do Shell e está associado somente ao aplicativo Paint.

![captura de tela mostrando o Explorer abrindo uma imagem sem nenhum tipo de arquivo](images/file-assoc/fileassoc-filetypehandler.png)

O arquivo deserto. known na captura de tela anterior não tem a seguinte funcionalidade habilitada por um manipulador de tipo de arquivo:

-   Miniatura ou visualização
-   Verbos específicos de imagem no menu de atalho, como:
    -   Girar visualização
    -   Definir como plano de fundo da área de trabalho
    -   Imprimir
-   Propriedades específicas da imagem no painel de **detalhes** , como:
    -   Data de início
    -   Marcações
    -   Classificação
-   Indexação do texto do arquivo

Na captura de tela a seguir, o mesmo arquivo (deserto. known) tem a extensão. jpg, que é um tipo de arquivo registrado que tem manipuladores de tipo de arquivo associados, portanto, uma imagem em miniatura e mais propriedades são mostradas.

![imagem com um tipo de arquivo registrado e manipuladores de tipo de arquivo associados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descrições do manipulador de tipo de arquivo

A funcionalidade fornecida por cada manipulador de tipo de arquivo está listada na tabela a seguir:



| Manipulador                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menu de atalho](context-menu-handlers.md)                   | Um manipulador de menu de atalho, às vezes chamado de manipulador de menu de contexto, é um manipulador de tipo de arquivo que adiciona comandos a um menu de contexto existente. Esses manipuladores estão associados a um determinado tipo de arquivo e são chamados sempre que um menu de contexto é exibido para um membro do tipo de arquivo.                                                                                                                                                                                                                                                                           |
| [Thumbnail](thumbnail-providers.md)                         | Um manipulador que fornece uma imagem para representar um item de Shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Propriedade](../properties/building-property-handlers-properties.md) | Um manipulador de propriedades que fornece acesso às propriedades do item para o Windows Search, o Windows Explorer e outros aplicativos que precisam acessar propriedades.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Visualização](preview-handlers.md)                              | Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item a ser exibido no painel de visualização do Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtros](../search/-search-3x-wds-extidx-filters.md)              | Um filtro, uma implementação da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , que examina os documentos em busca de texto e Propriedades (também chamados de atributos). Ele extrai partes do texto desses documentos, filtrando a formatação inserida e mantendo as informações sobre a posição do texto. Ele também extrai partes de valores, que são propriedades de um documento inteiro ou de partes bem definidas de um documento. O **IFilter** fornece a base para a criação de aplicativos de nível superior, como indexadores de documentos e visualizadores independentes de aplicativos. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
