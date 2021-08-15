---
description: Registrar um tipo de arquivo é a primeira etapa na criação de uma associação de arquivo, o que torna esse tipo de arquivo &\# 0034;conhecido&\# 0034; para o Shell. No entanto, sem manipuladores de tipo de arquivo, o Shell não pode expor informações ao usuário de e sobre o arquivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Manipuladores de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404cfd3be4c3e8a600b2f943bda1243ca243b70af411e104000245edd13d94c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459718"
---
# <a name="file-type-handlers"></a>Manipuladores de tipo de arquivo

[Registrar um tipo de arquivo](fa-how-work.md) é a primeira etapa na criação de uma associação de arquivo, o que torna esse tipo de arquivo "conhecido" para o Shell. No entanto, sem manipuladores de tipo de arquivo, o Shell não pode expor informações ao usuário de e sobre o arquivo.

Este tópico é organizado da seguinte forma:

-   [Tornar um tipo de arquivo conhecido como Shell](#make-a-file-type-known-to-shell)
-   [Descrições do manipulador de tipos de arquivo](#file-type-handler-descriptions)
-   [Tópicos relacionados](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Tornar um tipo de arquivo conhecido como Shell

Na captura de tela a seguir do Windows Explorer, o arquivo de imagem Explorer.known aparece na biblioteca **de** Imagens do Shell e está associado somente ao Paint aplicativo.

![captura de tela mostrando o explorer abrindo uma imagem sem tipo de arquivo](images/file-assoc/fileassoc-filetypehandler.png)

O arquivo Protocol.known na captura de tela anterior não tem a seguinte funcionalidade habilitada por um manipulador de tipo de arquivo:

-   Miniatura ou versão prévia
-   Verbos específicos da imagem no menu de atalho, como:
    -   Girar versão prévia
    -   Definir como Plano de Fundo da Área de Trabalho
    -   Imprimir
-   Propriedades específicas da imagem no **painel** Detalhes, como:
    -   Data de tomada
    -   Marcas
    -   Classificação
-   Indexação de texto do arquivo

Na captura de tela a seguir, o mesmo arquivo (File.known) tem a extensão .jpg, que é um tipo de arquivo registrado que tem manipuladores de tipo de arquivo associados, portanto, uma imagem em miniatura e mais propriedades são mostradas.

![imagem com um tipo de arquivo registrado e manipuladores de tipo de arquivo associados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descrições do manipulador de tipos de arquivo

A funcionalidade fornecida por cada manipulador de tipo de arquivo é listada na tabela a seguir:



| Manipulador                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menu de atalho](context-menu-handlers.md)                   | Um manipulador de menu de atalho, às vezes chamado de manipulador de menu de contexto, é um manipulador de tipo de arquivo que adiciona comandos a um menu de contexto existente. Esses manipuladores são associados a um tipo de arquivo específico e são chamados sempre que um menu de contexto é exibido para um membro do tipo de arquivo.                                                                                                                                                                                                                                                                           |
| [Thumbnail](thumbnail-providers.md)                         | Um manipulador que fornece uma imagem para representar um item do Shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Propriedade](../properties/building-property-handlers-properties.md) | Um manipulador de propriedades que fornece acesso às propriedades do item para Windows Search, o Windows Explorer e outros aplicativos que precisam acessar propriedades.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Visualização](preview-handlers.md)                              | Um manipulador que produz rapidamente uma exibição simplificada e somente leitura do item a ser exibido no painel de visualização Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtros](../search/-search-3x-wds-extidx-filters.md)              | Um filtro, uma implementação da interface [**IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) que examina documentos em busca de texto e propriedades (também chamados de atributos). Ele extrai partes de texto desses documentos, filtrando a formatação inserida e retendo informações sobre a posição do texto. Ele também extrai partes de valores, que são propriedades de um documento inteiro ou de partes bem definidas de um documento. **O IFilter** fornece a base para a criação de aplicativos de nível superior, como indexadores de documentos e visualizadores independentes de aplicativos. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro de aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivos](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de Tipo de Arquivo](file-type-verifier.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos percebidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
