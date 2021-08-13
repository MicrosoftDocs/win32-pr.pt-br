---
title: Fluxos arbitrário
description: Fluxos arbitrário
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows SDK do formato de mídia, fluxos arbitrários
- ASF (Advanced Systems Format), fluxos arbitrários
- ASF (formato de sistemas avançados), fluxos arbitrários
- Windows SDK do formato de mídia, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
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
# <a name="arbitrary-streams"></a>Fluxos arbitrário

Além dos fluxos de áudio e vídeo e fluxos de imagem, um arquivo ASF pode acomodar fluxos contendo uma variedade de dados. os objetos do SDK do formato de mídia Windows fornecem suporte para fluxos de script, fluxos de transferência de arquivo, fluxos da Web e fluxos de dados arbitrários. Todos esses tipos de fluxo são arbitrários, o que significa que nenhuma validação de dados é executada pelo objeto de leitura. Quando você inclui fluxos desses tipos em seus arquivos, certifique-se de que o aplicativo de leitura executa a validação ou verificação de dados para garantir que o conteúdo não tenha sido corrompido ou desconfigurado intencionalmente por terceiros mal-intencionados.

Embora os objetos desse SDK não verifiquem ou validem dados em fluxos arbitrários, vários tipos de fluxos arbitrários têm suporte nativo. A tabela a seguir lista os tipos de fluxo arbitrários predefinidos. Fluxos de script também têm suporte, mas são discutidos separadamente na seção [comandos de script](script-commands.md) . para obter mais informações sobre como criar tipos personalizados, consulte [Fluxos de dados arbitrários personalizados](custom-arbitrary-data-streams.md).



| Tipo arbitrário                   | Descrição                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Fluxos de texto](text-streams.md) | Conter cadeias de caracteres de texto.                                             |
| [Fluxos de arquivo](file-streams.md) | Conter um ou mais arquivos de dados.                                   |
| [Fluxos Web](web-streams.md)   | Conter arquivos de dados equivalentes à versão armazenada em cache das páginas da Web. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Fluxos de áudio e vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




