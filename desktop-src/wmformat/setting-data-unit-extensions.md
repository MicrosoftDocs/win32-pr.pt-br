---
title: Definindo extensões de unidade de dados
description: Definindo extensões de unidade de dados
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- extensões de unidade de dados, configurando
- fluxos, extensões de unidade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104499002"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="cbd1b-107">Definindo extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="cbd1b-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="cbd1b-108">Alguns fluxos são configurados para usar extensões de unidade de dados para associar dados complementares a exemplos individuais.</span><span class="sxs-lookup"><span data-stu-id="cbd1b-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="cbd1b-109">Para obter mais informações sobre amostras estendidas, consulte [extensões de unidade de dados](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="cbd1b-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="cbd1b-110">A maioria dos sistemas de extensão de unidade de dados requer uma extensão em cada exemplo no fluxo.</span><span class="sxs-lookup"><span data-stu-id="cbd1b-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="cbd1b-111">Se você não fornecer uma extensão do tamanho correto, o gravador rejeitará o exemplo.</span><span class="sxs-lookup"><span data-stu-id="cbd1b-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="cbd1b-112">Para adicionar dados estendidos a um exemplo, use o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="cbd1b-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="cbd1b-113">Você pode obter informações sobre as extensões de unidade de dados configuradas em um fluxo usando os métodos [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="cbd1b-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd1b-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbd1b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd1b-115">**Configurar extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="cbd1b-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="cbd1b-116">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="cbd1b-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




