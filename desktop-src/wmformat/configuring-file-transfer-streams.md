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
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="9efc1-109">Configurando fluxos de transferência de arquivo</span><span class="sxs-lookup"><span data-stu-id="9efc1-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="9efc1-110">Os fluxos de transferência de arquivo não exigem configurações especiais na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="9efc1-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="9efc1-111">Eles exigem uma extensão de unidade de dados para associar um nome de arquivo a cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="9efc1-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="9efc1-112">Para enviar um nome com exemplos de transferência de arquivo, você deve implementar um sistema de extensão de unidade de dados para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="9efc1-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="9efc1-113">Para definir uma extensão de unidade de dados para o fluxo, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="9efc1-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="9efc1-114">Obtenha um ponteiro para a interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) do objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9efc1-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="9efc1-115">Adicione uma extensão de unidade de dados para o fluxo chamando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9efc1-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9efc1-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9efc1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9efc1-117">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="9efc1-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="9efc1-118">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="9efc1-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="9efc1-119">**Fluxos de arquivos**</span><span class="sxs-lookup"><span data-stu-id="9efc1-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




