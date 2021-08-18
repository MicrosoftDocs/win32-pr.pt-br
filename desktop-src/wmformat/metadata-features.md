---
title: Recursos de metadados
description: Os metadados são usados em arquivos ASF para descrever o conteúdo e as propriedades do arquivo.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows SDK do formato de mídia, recursos de metadados
- Windows SDK do formato de mídia, recursos
- ASF (Advanced Systems Format), recursos de metadados
- ASF (formato de sistemas avançados), recursos de metadados
- ASF (Advanced Systems Format), recursos
- ASF (formato de sistemas avançados), recursos
- metadados, recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6865e54f2eeabcb96dd88df27aba578a9169ed84857d17af5602848041f24118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700448"
---
# <a name="metadata-features"></a>Recursos de metadados

Os metadados são usados em arquivos ASF para descrever o conteúdo e as propriedades do arquivo. Todos os arquivos ASF que você criar deverão incluir metadados apropriados. (Para obter uma visão geral, consulte [metadados](metadata.md).) o SDK do formato de mídia Windows inclui suporte para a edição de metadados por meio do objeto writer, o objeto editor de metadados e os objetos leitor e leitor síncrono. O suporte nativo para uma ampla variedade de atributos de metadados está incluído. Consulte [atributos](attributes.md) para obter uma lista dos atributos predefinidos.

o suporte de metadados fornecido pelos vários objetos do SDK do formato de mídia Windows é flexível e poderoso. Os principais recursos de metadados são resumidos na lista a seguir:

-   Tamanho de atributo flexível. Os atributos de metadados não são limitados em tamanho.
-   Atributos de nível de fluxo. Os metadados em arquivos ASF podem ser atribuídos ao arquivo como um todo ou a um fluxo específico.
-   Atributos duplicados. Um atributo nomeado pode ser usado várias vezes no mesmo arquivo. Esse recurso é específico para uso durante a atribuição de atributos descritivos de conteúdo. Por exemplo, uma música pode ter vários autores, cada um exigindo um atributo de **autor** separado no arquivo.
-   Vários idiomas. Cada atributo tem um idioma associado a ele. Você pode definir os idiomas com suporte e, em seguida, atribuir um para cada atributo que você escreve. Como você pode duplicar atributos, você pode fornecer os atributos mais importantes em várias linguagens para alcançar um público maior. Se você não especificar um idioma, o idioma padrão (obtido do sistema operacional do computador que executa o aplicativo) será usado.
-   Atributos complexos. Alguns dos atributos predefinidos dão suporte a dados estruturados. Para esses atributos, o tipo de dados é binary, mas o valor é uma estrutura definida neste SDK.

Os tópicos a seguir abordam os outros recursos de metadados com suporte.



| Tópico                                  | Descrição                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Suporte a ID3](id3.md)                 | discute o suporte para quadros ID3 usando os objetos do SDK do formato de mídia Windows. |
| [Metadados personalizados](custom-metadata.md) | Discute as implicações do uso de metadados personalizados.                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos**](features.md)
</dt> <dt>

[**Interface IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interface IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**Interface IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadados**](metadata.md)
</dt> </dl>

 

 




