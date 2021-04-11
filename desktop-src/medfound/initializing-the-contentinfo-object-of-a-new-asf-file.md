---
description: Inicializando o objeto ContentInfo de um novo arquivo ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inicializando o objeto ContentInfo de um novo arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74826942700f4be8028075fcd9466414834eb8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296315"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inicializando o objeto ContentInfo de um novo arquivo ASF

Depois de criar um objeto ContentInfo vazio chamando a função [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , o aplicativo deve chamar [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para fornecer o perfil de codificação. Para obter informações sobre como criar um perfil, consulte [criando um perfil ASF](creating-an-asf-profile.md).

Antes que as informações possam ser lidas do perfil, o método **setprofile** deve validar o objeto de perfil especificado verificando os identificadores de fluxo ou os tipos de mídia. Se o perfil passar na validação, vários objetos de cabeçalho serão gerados, como o objeto Propriedades de arquivo, o objeto Propriedades de taxa de bits de fluxo, o objeto Propriedades de fluxo e o objeto de exclusão mútua.

**Setprofile** calcula e define os valores recomendados para determinadas propriedades, como o valor de preroll. Se isso ainda não estiver definido, o valor de preroll recomendado em milissegundos dependerá da janela de buffer máximo do Bucket de vazamento especificado para os fluxos no perfil. Da mesma forma, os tamanhos mínimo e máximo de pacotes de dados também são definidos. Os valores recomendados podem substituir os tamanhos de pacotes definidos no perfil por meio de atributos.

Como o arquivo está no processo de ser criado, o arquivo é Categorizado como um tipo de difusão, indicado pelo campo sinalizadores do objeto Propriedades do arquivo. Determinados valores desconhecidos, como o número de pacotes de dados, duração da reprodução e duração de envio são definidos como zero. Esses valores são representados por atributos **MF \_ PD \_ ASF \_ xxx** e devem ser atualizados pelo aplicativo após a conclusão da criação do arquivo.

O objeto de perfil especificado substitui qualquer perfil existente associado ao objeto ContentInfo, remove os objetos de cabeçalho referenciados e redefine as propriedades de arquivo global, como preroll e o tamanho do pacote de dados.

O método **setprofile** também cria o objeto de dados que representa o objeto de dados ASF. Se você reutilizar um objeto ContentInfo que inclui informações sobre quaisquer pacotes de dados, **setprofile** falhará e retornará o \_ erro MF e \_ já \_ inicializado indicando que ele já está associado a um objeto de dados ASF existente. Por padrão, para um novo objeto ContentInfo, a contagem de pacotes de dados é definida como zero e o tamanho do objeto de dados é definido como 50 bytes. Se você usar o multiplexador para gerar pacotes de dados, o multiplexador atualizará o objeto ContentInfo para refletir os novos valores, como a contagem de pacotes de dados. Para obter mais informações sobre a geração de pacotes de dados, consulte [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).

Depois que todos os objetos de cabeçalho são adicionados ao objeto de cabeçalho ASF final, o tamanho total do cabeçalho pode ser recuperado chamando [**IMFASFContentInfo:: Getheadize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Esse tamanho inclui o tamanho inicial do objeto de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Gravando um objeto de cabeçalho ASF para um novo arquivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



