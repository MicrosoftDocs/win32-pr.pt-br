---
title: Dados arbitrários Fluxos
description: Dados arbitrários Fluxos
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows SDK de Formato de Mídia, fluxos arbitrários
- ASF (Advanced Systems Format), fluxos arbitrários
- ASF (Formato de Sistemas Avançados), fluxos arbitrários
- Windows SDK de Formato de Mídia, fluxos
- ASF (Advanced Systems Format), streams
- ASF (Formato de Sistemas Avançados), fluxos
- fluxos arbitrários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2cc0587758af8dfa3d4ee05b1a51943a89684629fe2182f5a33fdabbdb68e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434712"
---
# <a name="arbitrary-streams"></a>Dados arbitrários Fluxos

Além de fluxos de áudio e vídeo e fluxos de imagem, um arquivo ASF pode acomodar fluxos que contêm uma variedade de dados. Os objetos do SDK Windows Formato de Mídia fornecem suporte para fluxos de script, fluxos de transferência de arquivos, fluxos da Web e fluxos de dados arbitrários. Todos esses tipos de fluxo são arbitrários, o que significa que nenhuma validação de dados é executada pelo objeto de leitura. Quando você incluir fluxos desses tipos em seus arquivos, verifique se o aplicativo de leitura executa validação ou verificação de dados para garantir que seu conteúdo não tenha sido corrompido ou intencionalmente danificado por terceiros mal-intencionados.

Embora os objetos desse SDK não verifiquem ou validem dados em fluxos arbitrários, vários tipos de fluxos arbitrários têm suporte nativo. A tabela a seguir lista os tipos de fluxo arbitrários predefinidos. Os fluxos de script também têm suporte, mas são discutidos separadamente na seção [Comandos de](script-commands.md) Script. Para obter mais informações sobre como criar tipos personalizados, consulte [Dados arbitrários personalizados Fluxos](custom-arbitrary-data-streams.md).



| Tipo arbitrário                   | Descrição                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Texto Fluxos](text-streams.md) | Contêm cadeias de caracteres de texto.                                             |
| [Arquivos Fluxos](file-streams.md) | Contêm um ou mais arquivos de dados.                                   |
| [Web Fluxos](web-streams.md)   | Contêm arquivos de dados equivalentes à versão armazenada em cache de páginas da Web. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Áudio e vídeo Fluxos**](audio-and-video-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




