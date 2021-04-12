---
description: Este tópico descreve como trabalhar com perfis ASF no Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501202"
---
# <a name="asf-profile"></a>Perfil ASF

Este tópico descreve como trabalhar com perfis ASF no Microsoft Media Foundation.

Um arquivo ASF (Advanced Systems Format) contém um ou mais fluxos. Para cada fluxo, o cabeçalho ASF contém um cabeçalho de propriedades de fluxo que descreve o fluxo. Na camada [WMContainer](wmcontainer-asf-components.md) , os seguintes objetos são usados para definir ou ler as propriedades dos fluxos ASF:

-   Objeto de *perfil ASF* : descreve os fluxos e suas relações entre si. O objeto de perfil ASF expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .
-   Objeto de *configuração de fluxo* : descreve um fluxo. O objeto de configuração de fluxo contém um tipo de mídia que descreve o formato do fluxo. Para fluxos de áudio e vídeo, o tipo de mídia descreve exatamente como o fluxo é configurado e é usado por codecs que codificam ou decodificam o fluxo. O objeto de configuração de fluxo expõe a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Um perfil ASF válido contém pelo menos um objeto de configuração de fluxo.
-   Objeto de *exclusão mútua* : descreve vários fluxos que não devem ser lidos simultaneamente. Um objeto de exclusão mútua expõe a interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) . Um perfil ASF contém zero ou mais objetos de exclusão mútua.

O diagrama a seguir mostra a relação entre o perfil ASF e os objetos contidos no perfil.

![diagrama de árvore de um nó de perfil ASF com nós filho de configuração de fluxo; o primeiro aponta para o tipo de mídia, os próximos dois para a exclusão mútua](images/asf-components02.png)

Para reprodução, o perfil ASF é usado para enumerar os fluxos e localizar os formatos de fluxo. Para codificação, o perfil ASF é usado para configurar os fluxos no arquivo de destino.

O perfil ASF também é usado para configurar o [coletor de mídia ASF](asf-media-sinks.md). Para cada fluxo no perfil ASF, o coletor de mídia ASF cria um coletor de fluxo correspondente.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                           | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Criando um perfil ASF](creating-an-asf-profile.md)<br/>                               | Descreve como criar um objeto de perfil ASF.<br/>          |
| [Criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md)<br/>     | Descreve como adicionar fluxos a um perfil ASF.<br/>         |
| [Usando a exclusão mútua para fluxos ASF](using-mutual-exclusion-for-asf-streams.md)<br/> | Descreve como adicionar exclusões mútuas a fluxos ASF. <br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[Tutorial: 1-transmitir codificação de mídia do Windows](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[Tutorial: gravando um arquivo WMA usando a codificação de CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Componentes ASF WMContainer](wmcontainer-asf-components.md)
</dt> </dl>

 

 




