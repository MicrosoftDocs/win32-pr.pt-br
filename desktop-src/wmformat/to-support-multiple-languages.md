---
title: Dar suporte a várias linguagens
description: Dar suporte a várias linguagens
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows SDK de Formato de Mídia, dando suporte a vários idiomas
- Windows SDK de Formato de Mídia, suporte a vários idiomas
- Windows SDK de Formato de Mídia, suporte à linguagem
- ASF (Advanced Systems Format), dando suporte a vários idiomas
- ASF (Formato de Sistemas Avançados), dando suporte a vários idiomas
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (Formato de Sistemas Avançados), suporte a vários idiomas
- ASF (Advanced Systems Format), suporte à linguagem
- ASF (Formato de Sistemas Avançados), suporte à linguagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa610d5a9b0c92fb205ecdc234a18d816190223b5bca843a542e7222695fa24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699097"
---
# <a name="to-support-multiple-languages"></a>Dar suporte a várias linguagens

Você pode dar suporte a vários idiomas em fluxos e em metadados. O núcleo do suporte a vários idiomas no SDK Windows Media Format é a interface [**IWMLanguageList,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) que mantém uma lista dos idiomas com suporte. A lista de idiomas fornece a cada idioma com suporte um índice, que é usado em vários objetos no SDK ao lidar com vários idiomas.

O [**método IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) adiciona um idioma à lista. Você pode identificar os idiomas já na lista obtendo o número total de idiomas com [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e, em seguida, loop pelos idiomas que chamam [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada um. O índice de idioma é baseado em zero.

## <a name="to-configure-mutual-exclusion-by-language"></a>Para configurar a exclusão mútua por idioma

Configurar um objeto de exclusão mútua simples por idioma é muito simples. Cada fluxo agora está associado a um idioma. A linguagem associada a um fluxo pode ser definida usando [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage). Depois que todos os fluxos mutuamente exclusivos são configurados, basta criar um objeto de exclusão mútua como faria para qualquer outro tipo. Em seguida, [**chame IWMMutualExclusion::SetType passando**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) CLSID \_ WMMUTEX \_ Language para o tipo.

Fluxos que são mutuamente exclusivos por idioma tornam-se mais complicados quando os fluxos exclusivos também são mutuamente exclusivos por taxa de bits. Nesse caso, você deve usar registros mutuamente exclusivos, executando as seguintes etapas:

1.  Crie um objeto de exclusão mútua para os fluxos de taxas de bits diferentes em cada idioma. Para obter mais informações sobre como criar um objeto de exclusão mútua por taxa de bits, consulte [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).
2.  Crie um objeto de exclusão mútua. Chame [**IWMMutualExclusion::SetType e**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passe CLSID WMMUTEX Language para especificar \_ a exclusividade por \_ idioma.
3.  Obtenha um ponteiro para a interface [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) do objeto de exclusão mútua criado na etapa 2 chamando o método **QueryInterface** [**de IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).
4.  Chame o [**método IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) uma vez para cada idioma, para criar registros de fluxo que serão mutuamente exclusivos.
5.  Para cada registro criado na etapa 4, adicione os fluxos do idioma apropriado com chamadas para [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).

## <a name="to-read-files-with-multiple-languages"></a>Para ler arquivos com vários idiomas

O objeto leitor fornece métodos para identificar os idiomas disponíveis de fluxos em um arquivo. Você pode recuperar o número de idiomas com suporte para uma saída chamando [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount). Em seguida, você pode recuperar detalhes sobre cada idioma com chamadas para [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).

Você pode especificar o idioma a ser reproduzir passando o índice desse idioma para o leitor com uma chamada para [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting). Isso selecionará o idioma especificado, mantendo a seleção automática de fluxo para qualquer outro objeto de exclusão mútua no arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**IWMLanguageList Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[**IWMMutualExclusion Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMMutualExclusion2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[**IWMReaderAdvanced2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMReaderAdvanced4 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[**IWMStreamConfig3 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




