---
description: descreve como adicionar extensões de unidade de dados ao usar Windows codificadores de mídia.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Usando extensões de unidade de dados (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4680626f06c93e63f293699360d98ac995eedc3b3351fe617c182dbc176165ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972715"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Usando extensões de unidade de dados (Microsoft Media Foundation)

os codecs de áudio e vídeo de mídia Windows são projetados para funcionar bem com o contêiner ASF (Advanced Systems Format). o ASF é o formato estruturado usado para arquivos WMA (Windows media Audio) e arquivos WMV (Windows media Video). É um formato extensível projetado para dados de streaming. Uma das características incomuns da estrutura do ASF é a capacidade de anexar metadados a exemplos individuais e inserir esses dados com os exemplos no fluxo de bits. Um item de metadados armazenados dessa maneira é chamado de extensão de *unidade* de dados ou *extensão de exemplo*.

Uma extensão de unidade de dados pode conter informações necessárias para o codificador, o decodificador ou o aplicativo de Player. a maioria dos tipos de extensão de unidade de dados que são implementados na série Windows Media 9 de codecs contém dados destinados ao aplicativo que decodifica e renderiza a mídia. Por exemplo, você pode manter os códigos de tempo SMPTE dos dados de origem adicionando-os como extensões de unidade de dados. No entanto, os seguintes recursos de codec exigem extensões de unidade de dados:

-   [Inserção de quadro-chave forçada](forcedkeyframeinsertion.md)
-   [Codificação de vídeo entrelaçado](interlacedvideoencoding.md)
-   A dificuldade de usar as extensões de unidade de dados ao acessar o codec diretamente é o mecanismo pelo qual o objeto recebe os dados de extensão. isso é obtido pelos objetos do SDK do formato de mídia Windows usando objetos de buffer projetados para dar suporte a esse recurso. é recomendável que você use o SDK do formato de mídia Windows para ativar os recursos de codec que exigem extensões de unidade de dados, mas você pode fazer com que esses recursos funcionem com os objetos de codec autônomos.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Passando amostras estendidas para os objetos de codec

o SDK do formato de mídia Windows usa objetos de buffer que expõem interfaces [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) . A interface mais recente é [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Para passar amostras para um objeto de codec com extensões de unidade de dados, você deve usar um objeto de buffer que implementa a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) ou [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) e a interface **INSSBuffer** . você pode usar objetos de buffer criados pelo SDK do formato de mídia Windows ou Microsoft Media Foundation para fazer isso, ou pode criar sua própria classe de buffer que atenda aos requisitos. Para criar sua própria classe de buffer, você deve estar em conformidade com os protótipos de método para as interfaces **INSSBuffer** . essas definições de interface podem ser encontradas no arquivo de cabeçalho wmsbuffer. h instalado com o SDK do formato de mídia Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 
