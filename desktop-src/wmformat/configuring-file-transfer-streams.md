---
title: configurando a transferência de arquivos Fluxos
description: configurando a transferência de arquivos Fluxos
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- fluxos, configurando fluxos de transferência de arquivo
- codecs, configurando fluxos de transferência de arquivo
- fluxos de transferência de arquivo
- fluxos, extensões de unidade de dados
- codecs, extensões de unidade de dados
- extensões de unidade de dados, fluxos de transferência de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849059"
---
# <a name="configuring-file-transfer-streams"></a>configurando a transferência de arquivos Fluxos

Os fluxos de transferência de arquivo não exigem configurações especiais na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Eles exigem uma extensão de unidade de dados para associar um nome de arquivo a cada exemplo. Para enviar um nome com exemplos de transferência de arquivo, você deve implementar um sistema de extensão de unidade de dados para o fluxo.

Para definir uma extensão de unidade de dados para o fluxo, execute as seguintes etapas:

1.  Obtenha um ponteiro para a interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.
2.  Adicione uma extensão de unidade de dados para o fluxo chamando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) da seguinte maneira:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos de arquivo**](file-streams.md)
</dt> </dl>

 

 




