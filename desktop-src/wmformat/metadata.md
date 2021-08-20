---
title: Metadados
description: Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows SDK do formato de mídia, visão geral de metadados
- ASF (Advanced Systems Format), visão geral dos metadados
- ASF (formato de sistemas avançados), visão geral dos metadados
- metadados, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad8a687db3fc21c6d73ee43e4f6530fd6e2e504433699f4619ee3165c7af0fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846441"
---
# <a name="metadata"></a>Metadados

Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo. A seção de cabeçalho de um arquivo ASF contém todos os metadados associados a esse arquivo. Itens individuais de metadados em um arquivo ASF são chamados de atributos. Cada atributo tem um nome e um valor. Ao longo desta documentação, constantes globais são usadas para identificar atributos. Por exemplo, o título de um arquivo ASF é armazenado no atributo **g \_ wszWMTitle** .

vários atributos são definidos no SDK do formato de mídia Windows para lidar com as necessidades de metadados mais comuns. Além disso, você pode criar seus próprios atributos. No entanto, você deve tomar cuidado ao nomear atributos personalizados porque outros desenvolvedores de aplicativos podem usar os mesmos nomes e os conflitos podem ocorrer.

Alguns atributos são definidos pelo SDK e não podem ser alterados manualmente. Por exemplo, quando você indexa um arquivo ASF, o SDK define o atributo **g \_ wszWMSeekable** para mostrar que o arquivo agora pode ser lido de qualquer ponto especificado.

Outros atributos são puramente informativos e devem ser definidos manualmente. Por exemplo, se você quiser controlar o autor de um arquivo, defina **g \_ wszWMAuthor**.

o SDK do formato de mídia Windows fornece suporte para atributos que se aplicam a todo o arquivo e atributos que se aplicam a fluxos individuais.

você pode usar o SDK do formato de mídia Windows para editar os metadados em arquivos mp3, embora você sempre deva usar atributos em conformidade com ID3 em arquivos mp3 para manter a compatibilidade com outros programas de manipulação de MP3.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Objeto do editor de metadados**](metadata-editor-object.md)
</dt> <dt>

[**Recursos de metadados**](metadata-features.md)
</dt> <dt>

[**Trabalhando com metadados**](working-with-metadata.md)
</dt> </dl>

 

 




