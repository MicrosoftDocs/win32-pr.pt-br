---
description: Descreve como adicionar extensões de unidade de dados ao usar codificadores de mídia do Windows.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Usando extensões de unidade de dados (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754083"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Usando extensões de unidade de dados (Microsoft Media Foundation)

Os codecs de áudio e vídeo do Windows Media são projetados para funcionar bem com o contêiner ASF (Advanced Systems Format). O ASF é o formato estruturado usado para arquivos de áudio do Windows Media (WMA) e de vídeo do Windows Media (WMV). É um formato extensível projetado para dados de streaming. Uma das características incomuns da estrutura do ASF é a capacidade de anexar metadados a exemplos individuais e inserir esses dados com os exemplos no fluxo de bits. Um item de metadados armazenados dessa maneira é chamado de extensão de *unidade* de dados ou *extensão de exemplo*.

Uma extensão de unidade de dados pode conter informações necessárias para o codificador, o decodificador ou o aplicativo de Player. A maioria dos tipos de extensão de unidade de dados que são implementados na série de codecs do Windows Media 9 contém dados destinados ao aplicativo que decodifica e renderiza a mídia. Por exemplo, você pode manter os códigos de tempo SMPTE dos dados de origem adicionando-os como extensões de unidade de dados. No entanto, os seguintes recursos de codec exigem extensões de unidade de dados:

-   [Inserção de quadro-chave forçada](forcedkeyframeinsertion.md)
-   [Codificação de vídeo entrelaçado](interlacedvideoencoding.md)
-   A dificuldade de usar as extensões de unidade de dados ao acessar o codec diretamente é o mecanismo pelo qual o objeto recebe os dados de extensão. Isso é obtido pelos objetos do SDK do Windows Media Format usando objetos de buffer projetados para dar suporte a esse recurso. É recomendável que você use o Windows Media Format SDK para ativar os recursos de codec que exigem extensões de unidade de dados, mas você pode fazer com que esses recursos funcionem com os objetos de codec autônomos.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Passando amostras estendidas para os objetos de codec

O Windows Media Format SDK usa objetos de buffer que expõem interfaces [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) . A interface mais recente é [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Para passar amostras para um objeto de codec com extensões de unidade de dados, você deve usar um objeto de buffer que implementa a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) ou [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) e a interface **INSSBuffer** . Você pode usar objetos de buffer criados pelo Windows Media Format SDK ou Microsoft Media Foundation para fazer isso, ou você pode criar sua própria classe de buffer que atenda aos requisitos. Para criar sua própria classe de buffer, você deve estar em conformidade com os protótipos de método para as interfaces **INSSBuffer** . Essas definições de interface podem ser encontradas no arquivo de cabeçalho wmsbuffer. h que é instalado com o Windows Media Format SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificações de mídia do Windows](windows-media-codecs.md)
</dt> </dl>

 

 
