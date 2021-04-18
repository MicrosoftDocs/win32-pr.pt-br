---
description: Objeto ASF ContentInfo
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Objeto ASF ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796064"
---
# <a name="asf-contentinfo-object"></a>Objeto ASF ContentInfo

O objeto ASF *ContentInfo* armazena informações do objeto de cabeçalho ASF de um arquivo. Um aplicativo pode usar o objeto ContentInfo para as seguintes finalidades:

-   Ler o objeto de cabeçalho para um arquivo de mídia existente. Nesse caso, o objeto ContentInfo analisa o objeto de cabeçalho e armazena informações sobre o arquivo de características. Media Foundation expõe várias dessas propriedades por meio de atributos e interfaces. Elas são descritas em [atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md).
-   Gravar informações de cabeçalho e construir um objeto de cabeçalho para um novo arquivo.
-   Inicialize outros objetos ASF, como o [divisor ASF](asf-splitter.md), o [multiplexador ASF](asf-multiplexer.md)e o indexador ASF, ao ler ou gravar um arquivo de mídia.

Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).

## <a name="creating-the-contentinfo-object"></a>Criando o objeto ContentInfo

Para criar uma nova instância do objeto ContentInfo, chame a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) . Esse método retorna um ponteiro para um objeto ContentInfo vazio que deve ser inicializado para funcionar com um arquivo ASF específico. Dependendo se o aplicativo está lendo um arquivo existente ou gravando um novo arquivo ASF, ele deve chamar [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) ou [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para preencher o objeto vazio.

Para obter mais informações sobre essas chamadas de método, consulte os seguintes tópicos:

-   [Lendo o objeto de cabeçalho ASF de um arquivo existente](reading-the-asf-header-object-of-an-existing-file.md)
-   [Obtendo informações de objetos de cabeçalho ASF](getting-information-from-asf-header-objects.md)
-   [Gravando um objeto de cabeçalho ASF para um novo arquivo](writing-an-asf-header-object-for-a-new-file.md)
-   [Atributos de Media Foundation para objetos de cabeçalho ASF](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 



