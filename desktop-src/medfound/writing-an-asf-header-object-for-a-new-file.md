---
description: Gravando um objeto de cabeçalho ASF para um novo arquivo
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: Gravando um objeto de cabeçalho ASF para um novo arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dfcaf0d7c7c4ca469e75fb4c1bd47a4f8b1d32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773017"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>Gravando um objeto de cabeçalho ASF para um novo arquivo

O objeto ASF ContentInfo armazena informações do objeto de cabeçalho ASF para um arquivo. Quando um arquivo ASF é criado ou modificado, o objeto de cabeçalho deve ser gerado. Para fazer isso, o aplicativo deve fornecer o perfil de codificação do conteúdo ao objeto ContentInfo para que ele saiba as características do arquivo de mídia a ser criado.

Para gravar um novo arquivo, você pode usar o objeto ContentInfo para:

-   Coletar informações de cabeçalho do objeto de perfil do arquivo a ser criado,
-   Preencher vários objetos de cabeçalho na biblioteca ASF mantidos internamente pelo Media Foundation,
-   Inicializar o [Multiplexador de ASF](asf-multiplexer.md) para geração de pacotes de dados ASF e
-   Construa o objeto de cabeçalho de nível superior no formato binário que pode ser gravado em um arquivo.

Para obter informações sobre perfis, consulte [perfil ASF](asf-profile.md).

Esta seção contém os seguintes tópicos:



| Tópico                                                                                                              | Descrição                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md) | Descreve o método [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) que inicializa o objeto ContentInfo com informações de cabeçalho armazenadas em um objeto de perfil. |
| [Definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)                   | Informações sobre várias propriedades de configuração que devem ser definidas no objeto ContentInfo.                                                                                         |
| [Gerando um novo objeto de cabeçalho ASF](generating-a-new-asf-header-object.md)                                       | Como gerar um buffer de mídia, que contém o objeto de cabeçalho ASF real do novo arquivo, a partir do objeto ContentInfo.                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objeto ASF ContentInfo](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

Estrutura de arquivo ASF
</dt> </dl>

 

 



