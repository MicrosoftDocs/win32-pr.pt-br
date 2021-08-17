---
title: Objeto de leitor síncrono
description: Objeto de leitor síncrono
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows SDK do formato de mídia, objetos de leitor síncronos
- ASF (Advanced Systems Format), objetos de leitor síncronos
- ASF (formato de sistemas avançados), objetos de leitor síncronos
- objetos, objetos de leitor síncronos
- leitores síncronos, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 629f08684f996a611acaf00b913eaa8715869bdfd0219ea27994e2f8faf7c896
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197056"
---
# <a name="synchronous-reader-object"></a>Objeto de leitor síncrono

O objeto leitor síncrono é usado para ler arquivos de mídia digital usando chamadas síncronas.

O objeto leitor síncrono é criado pela função [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), que define um ponteiro para uma interface **IWMSyncReader** . As outras interfaces com suporte da interface de leitor síncrona podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto leitor síncrono.



| Interface                                | Descrição                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Define e recupera informações de cabeçalho, como metadados, [*marcadores*](wmformat-glossary.md)e assim por diante.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Enumera as informações de codec disponíveis. Herda todos os métodos de **IWMHeaderInfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Dá suporte a tamanhos de atributos grandes, nomes de atributos duplicados e suporte a vários idiomas. Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**. |
| [**IWMProfile**](iwmprofile.md)         | fornece acesso às informações de perfil do arquivo de mídia Windows carregado no leitor.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Recupera o GUID (identificador global exclusivo), se houver, associado ao perfil. Herda todos os métodos de **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Dá suporte ao compartilhamento de largura de banda e às informações de priorização de fluxo no perfil. Herda todos os métodos de **IWMProfile** e **IWMProfile2**.                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Fornece recursos de leitura síncrona para arquivos de mídia digital.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Fornece suporte para a busca de códigos de tempo SMPTE e para alocar amostras manualmente. Herda todos os métodos de **IWMSyncReader**.                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto**](objects.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




