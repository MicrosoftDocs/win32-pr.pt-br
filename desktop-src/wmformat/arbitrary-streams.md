---
title: Fluxos arbitrários
description: Fluxos arbitrários
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- SDK do Windows Media Format, fluxos arbitrários
- ASF (Advanced Systems Format), fluxos arbitrários
- ASF (formato de sistemas avançados), fluxos arbitrários
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- fluxos arbitrários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635025"
---
# <a name="arbitrary-streams"></a>Fluxos arbitrários

Além dos fluxos de áudio e vídeo e fluxos de imagem, um arquivo ASF pode acomodar fluxos contendo uma variedade de dados. Os objetos do Windows Media Format SDK fornecem suporte para fluxos de script, fluxos de transferência de arquivos, fluxos da Web e fluxos de dados arbitrários. Todos esses tipos de fluxo são arbitrários, o que significa que nenhuma validação de dados é executada pelo objeto de leitura. Quando você inclui fluxos desses tipos em seus arquivos, certifique-se de que o aplicativo de leitura executa a validação ou verificação de dados para garantir que o conteúdo não tenha sido corrompido ou desconfigurado intencionalmente por terceiros mal-intencionados.

Embora os objetos desse SDK não verifiquem ou validem dados em fluxos arbitrários, vários tipos de fluxos arbitrários têm suporte nativo. A tabela a seguir lista os tipos de fluxo arbitrários predefinidos. Fluxos de script também têm suporte, mas são discutidos separadamente na seção [comandos de script](script-commands.md) . Para obter mais informações sobre como criar tipos personalizados, consulte [fluxos de dados arbitrários personalizados](custom-arbitrary-data-streams.md).



| Tipo arbitrário                   | Description                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Fluxos de texto](text-streams.md) | Conter cadeias de caracteres de texto.                                             |
| [Fluxos de arquivos](file-streams.md) | Conter um ou mais arquivos de dados.                                   |
| [Fluxos da Web](web-streams.md)   | Conter arquivos de dados equivalentes à versão armazenada em cache das páginas da Web. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Fluxos de áudio e vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




