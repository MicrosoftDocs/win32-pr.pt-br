---
title: Configurando fluxos de transferência de arquivo
description: Configurando fluxos de transferência de arquivo
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
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007149"
---
# <a name="configuring-file-transfer-streams"></a>Configurando fluxos de transferência de arquivo

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

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos de arquivos**](file-streams.md)
</dt> </dl>

 

 




