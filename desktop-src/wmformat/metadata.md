---
title: Metadados
description: Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- SDK do Windows Media Format, visão geral de metadados
- ASF (Advanced Systems Format), visão geral dos metadados
- ASF (formato de sistemas avançados), visão geral dos metadados
- metadados, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292763"
---
# <a name="metadata"></a>Metadados

Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo. A seção de cabeçalho de um arquivo ASF contém todos os metadados associados a esse arquivo. Itens individuais de metadados em um arquivo ASF são chamados de atributos. Cada atributo tem um nome e um valor. Ao longo desta documentação, constantes globais são usadas para identificar atributos. Por exemplo, o título de um arquivo ASF é armazenado no atributo **g \_ wszWMTitle** .

Vários atributos são definidos no Windows Media Format SDK para lidar com as necessidades de metadados mais comuns. Além disso, você pode criar seus próprios atributos. No entanto, você deve tomar cuidado ao nomear atributos personalizados porque outros desenvolvedores de aplicativos podem usar os mesmos nomes e os conflitos podem ocorrer.

Alguns atributos são definidos pelo SDK e não podem ser alterados manualmente. Por exemplo, quando você indexa um arquivo ASF, o SDK define o atributo **g \_ wszWMSeekable** para mostrar que o arquivo agora pode ser lido de qualquer ponto especificado.

Outros atributos são puramente informativos e devem ser definidos manualmente. Por exemplo, se você quiser controlar o autor de um arquivo, defina **g \_ wszWMAuthor**.

O Windows Media Format SDK fornece suporte para atributos que se aplicam a todo o arquivo e atributos que se aplicam a fluxos individuais.

Você pode usar o Windows Media Format SDK para editar os metadados em arquivos MP3, embora você sempre deva usar atributos em conformidade com ID3 em arquivos MP3 para manter a compatibilidade com outros programas de manipulação de MP3.

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

 

 




