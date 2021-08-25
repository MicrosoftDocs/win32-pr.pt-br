---
description: Usando o Localizador de Mídia
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Usando o Localizador de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be064a375f121f7c4e3dad54c2615bf8d6f7df489e119ec9cbb2c6f4b4294628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633126"
---
# <a name="using-the-media-locator"></a>Usando o Localizador de Mídia

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

O localizador de mídia é um objeto auxiliar que verifica nomes de arquivo e procura arquivos ausentes em diretórios locais ou de rede. O detector de mídia mantém um cache de caminhos de diretório em que ele encontrou arquivos com êxito em pesquisas anteriores. Para localizar um arquivo, ele pesquisa os diretórios em seu cache. Se isso não for feito, o detector de mídia poderá exibir uma caixa de diálogo Abrir Arquivo para que o usuário localize um arquivo manualmente. Supondo que o usuário localize o arquivo, o localizador de mídia adiciona o novo diretório ao cache. O localizador de mídia expõe a interface [**IMediaLocator.**](imedialocator.md)

Normalmente, seu aplicativo não cria diretamente uma instância do localizador de mídia. Em vez disso, a linha do tempo e o mecanismo de renderização fornecem os métodos a seguir para validar nomes de arquivo usando o detector de mídia.

-   Para validar nomes de arquivo na linha do tempo, chame [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md). Opcionalmente, esse método também atualiza os objetos de origem com os nomes de arquivo corretos.
-   Para validar nomes de arquivo quando o projeto for renderizado, chame [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Ambos os métodos têm sinalizadores que controlam o comportamento do localizador de mídia. Por exemplo, você pode restringir a pesquisa a diretórios locais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com fontes](working-with-sources.md)
</dt> </dl>

 

 



