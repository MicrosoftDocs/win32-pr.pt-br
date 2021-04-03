---
description: Usando o localizador de mídia
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Usando o localizador de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930091"
---
# <a name="using-the-media-locator"></a>Usando o localizador de mídia

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O localizador de mídia é um objeto auxiliar que verifica os nomes de arquivo e procura arquivos ausentes em diretórios locais ou de rede. O detector de mídia mantém um cache de caminhos de diretório onde encontrou com êxito os arquivos nas pesquisas anteriores. Para localizar um arquivo, ele pesquisa os diretórios em seu cache. Falhando, o detector de mídia pode exibir uma caixa de diálogo abrir arquivo para que o usuário localize um arquivo manualmente. Supondo que o usuário localize o arquivo, o localizador de mídia adiciona o novo diretório ao seu cache. O localizador de mídia expõe a interface [**IMediaLocator**](imedialocator.md) .

Normalmente, seu aplicativo não cria diretamente uma instância do localizador de mídia. Em vez disso, a linha do tempo e o mecanismo de processamento fornecem os métodos a seguir para validar nomes de arquivo usando o detector de mídia.

-   Para validar os nomes de arquivo na linha do tempo, chame [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md). Opcionalmente, esse método também atualiza os objetos de origem com os nomes de arquivo corretos.
-   Para validar nomes de arquivo quando o projeto é renderizado, chame [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Ambos os métodos usam sinalizadores que controlam o comportamento do localizador de mídia. Por exemplo, você pode restringir a pesquisa a diretórios locais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



