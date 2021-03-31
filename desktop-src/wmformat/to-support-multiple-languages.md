---
title: Dar suporte a várias linguagens
description: Dar suporte a várias linguagens
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- SDK do Windows Media Format, com suporte para vários idiomas
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, suporte a idiomas
- ASF (Advanced Systems Format), com suporte para vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- ASF (Advanced Systems Format), suporte a idiomas
- ASF (formato de sistemas avançados), suporte a idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103917066"
---
# <a name="to-support-multiple-languages"></a>Dar suporte a várias linguagens

Você pode dar suporte a vários idiomas em fluxos e em metadados. O núcleo de suporte a vários idiomas no Windows Media Format SDK é a interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , que mantém uma lista dos idiomas com suporte. A lista de idiomas fornece a cada idioma suportado um índice, que é usado em vários objetos no SDK ao lidar com vários idiomas.

O método [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) adiciona um idioma à lista. Você pode identificar os idiomas que já estão na lista obtendo o número total de idiomas com [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e, em seguida, fazendo um loop pelos idiomas chamando [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada um. O índice de idioma é baseado em zero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Para configurar a exclusão mútua por idioma

A configuração de um objeto de exclusão mútua simples por linguagem é muito simples. Cada fluxo agora está associado a um idioma. O idioma associado a um fluxo pode ser definido usando [**IWMStreamConfig3:: setlanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Depois que todos os fluxos mutuamente exclusivos são configurados, basta criar um objeto de exclusão mútua como você faria para qualquer outro tipo. Em seguida, chame [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passando \_ \_ o idioma WMMUTEX do CLSID para o tipo.

Os fluxos mutuamente exclusivos por idioma se tornam mais complicados quando os fluxos exclusivos também são mutuamente exclusivos por taxa de bits. Nesse caso, você deve usar registros mutuamente exclusivos, executando as seguintes etapas:

1.  Crie um objeto de exclusão mútua para os fluxos de taxas de bits diferentes em cada idioma. Para obter mais informações sobre como criar um objeto de exclusão mútua por taxa de bits, consulte [usando a exclusão mútua de taxa de bits múltipla](using-multiple-bit-rate-mutual-exclusion.md).
2.  Crie um objeto de exclusão mútua. Chame [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) e transmita o \_ idioma WMMUTEX do CLSID \_ para especificar exclusividade por idioma.
3.  Obtenha um ponteiro para a interface [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) do objeto de exclusão mútua criado na etapa 2 chamando o método **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Chame o método [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) uma vez para cada idioma, para criar registros de fluxo que serão mutuamente exclusivos.
5.  Para cada registro criado na etapa 4, adicione os fluxos do idioma apropriado com chamadas para [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Para ler arquivos com vários idiomas

O objeto leitor fornece métodos para identificar os idiomas disponíveis de fluxos em um arquivo. Você pode recuperar o número de idiomas com suporte para uma saída chamando [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). Em seguida, você pode recuperar detalhes sobre cada idioma com chamadas para [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Você pode especificar a linguagem a ser reproduzida passando o índice desse idioma para o leitor com uma chamada para [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Isso selecionará o idioma especificado enquanto mantém a seleção de fluxo automática para qualquer outro objeto de exclusão mútua no arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Interface IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**Interface IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interface IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**Interface IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




