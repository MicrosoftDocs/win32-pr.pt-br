---
description: Escrevendo um objeto de header ASF para um novo arquivo
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Escrevendo um objeto de header ASF para um novo arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee50adc4e3f411bca9679672b88680ab3064bc91d828e2897ae1f94e40f9f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355206"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Escrevendo um objeto de header ASF para um novo arquivo

O objeto ContentInfo do ASF armazena informações de Objeto de Header ASF para um arquivo. Quando um arquivo ASF é criado ou modificado, o Objeto de Header deve ser gerado. Para fazer isso, o aplicativo deve fornecer o perfil de codificação do conteúdo para o objeto ContentInfo para que ele saiba as características do arquivo de mídia a ser criado.

Para escrever um novo arquivo, você pode usar o objeto ContentInfo para:

-   Coletar informações de header do objeto de perfil do arquivo a ser criado,
-   Preencha vários objetos de header na biblioteca ASF mantidos internamente por Media Foundation,
-   Inicializar o [multiplexador ASF para](asf-multiplexer.md) geração de pacotes de dados ASF e
-   Construa o Objeto de Header de nível superior em formato binário que pode ser gravado em um arquivo.

Para obter informações sobre perfis, consulte [Perfil ASF](asf-profile.md).

Esta seção contém os seguintes tópicos:



| Tópico                                                                                                              | Descrição                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Descreve o [**método IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) que inicializa o objeto ContentInfo com informações de título armazenadas em um objeto de perfil. |
| [Definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Informações sobre várias propriedades de configuração que devem ser definidas no objeto ContentInfo.                                                                                         |
| [Gerando um novo objeto de header ASF](generating-a-new-asf-header-object.md)                                       | Como gerar um buffer de mídia, que contém o objeto de título ASF real do novo arquivo, do objeto ContentInfo.                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ContentInfo do ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> <dt>

Estrutura do arquivo ASF
</dt> </dl>

 

 



