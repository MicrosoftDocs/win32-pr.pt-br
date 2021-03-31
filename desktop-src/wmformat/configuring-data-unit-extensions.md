---
title: Configurar extensões de unidade de dados
description: Configurar extensões de unidade de dados
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- fluxos, configurando extensões de unidade de dados
- fluxos, extensões de unidade de dados
- extensões de unidade de dados, configurando
- perfis, extensões de unidade de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640285"
---
# <a name="configuring-data-unit-extensions"></a><span data-ttu-id="c14f5-107">Configurar extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="c14f5-107">Configuring Data Unit Extensions</span></span>

<span data-ttu-id="c14f5-108">Exemplos gravados em arquivos ASF podem conter informações adicionais além das amostras de mídia em si.</span><span class="sxs-lookup"><span data-stu-id="c14f5-108">Samples written to ASF files can contain additional information apart from the media samples themselves.</span></span> <span data-ttu-id="c14f5-109">Essas informações são incluídas usando as extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="c14f5-109">This information is included using data unit extensions.</span></span> <span data-ttu-id="c14f5-110">Para obter mais informações sobre extensões de unidade de dados, consulte [extensões de unidade de dados](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c14f5-110">For more information about data unit extensions, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="c14f5-111">Para usar extensões de unidade de dados, você deve configurar o fluxo no perfil para aceitá-los.</span><span class="sxs-lookup"><span data-stu-id="c14f5-111">To use data unit extensions, you must configure the stream in the profile to accept them.</span></span> <span data-ttu-id="c14f5-112">Para configurar uma extensão de unidade de dados para um fluxo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c14f5-112">To configure a data unit extension for a stream, perform the following steps.</span></span>

1.  <span data-ttu-id="c14f5-113">Obtenha um ponteiro para a interface [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) chamando o método **QueryInterface** de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="c14f5-113">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface by calling the **QueryInterface** method of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span>
2.  <span data-ttu-id="c14f5-114">Chame [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para registrar um tipo de extensão de unidade de dados para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="c14f5-114">Call [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) to register a type of data unit extension for the stream.</span></span>

<span data-ttu-id="c14f5-115">Você pode examinar todos os tipos de extensão de unidade de dados registrados atualmente para um fluxo chamando [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) para recuperar o número de tipos de extensão de unidade de dados registrados.</span><span class="sxs-lookup"><span data-stu-id="c14f5-115">You can examine all of the data unit extension types currently registered for a stream by calling [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) to retrieve the number of registered data unit extension types.</span></span> <span data-ttu-id="c14f5-116">Em seguida, você pode executar um loop por todos os tipos usando chamadas para [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) para cada.</span><span class="sxs-lookup"><span data-stu-id="c14f5-116">Then you can loop through all of the types using calls to [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) for each.</span></span>

<span data-ttu-id="c14f5-117">As extensões de unidade de dados recebem um tamanho quando configuradas para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="c14f5-117">Data unit extensions are assigned a size when configured for a stream.</span></span> <span data-ttu-id="c14f5-118">Muitos sistemas de extensão de unidade de dados usam dados que são um tamanho constante (geralmente uma estrutura).</span><span class="sxs-lookup"><span data-stu-id="c14f5-118">Many data unit extension systems use data that is a constant size (usually a structure).</span></span> <span data-ttu-id="c14f5-119">No entanto, você também pode configurar suas extensões de unidade de dados para que sejam do tamanho da variável, definindo o tamanho como 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="c14f5-119">However, you can also configure your data unit extensions to be of variable size by setting the size to 0xFFFF.</span></span> <span data-ttu-id="c14f5-120">Cada extensão de unidade de dados atribuída no momento da codificação pode ser de qualquer tamanho entre 1 byte e 65534 bytes.</span><span class="sxs-lookup"><span data-stu-id="c14f5-120">Each data unit extension assigned at encoding time can then be of any size between 1 byte and 65534 bytes.</span></span> <span data-ttu-id="c14f5-121">As extensões de unidade de dados de tamanho variados também são chamadas de extensões de unidade de dados dinâmicas</span><span class="sxs-lookup"><span data-stu-id="c14f5-121">Variably sized data unit extensions are also called dynamic data unit extensions.</span></span>

<span data-ttu-id="c14f5-122">A vantagem de usar extensões de unidade de dados dinâmicas é que você pode anexar dados de extensão conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="c14f5-122">The advantage of using dynamic data unit extensions is that you can attach extension data as needed.</span></span> <span data-ttu-id="c14f5-123">Se você definir uma extensão de unidade de dados com um tamanho definido, cada amostra do fluxo deverá conter dados de extensão desse tamanho, mesmo que você não tenha dados para alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="c14f5-123">If you define a data unit extension with a set size, every sample for the stream must contain extension data of that size, even if you have no data for some samples.</span></span> <span data-ttu-id="c14f5-124">Com extensões de unidade de dados dinâmicas, você pode omitir as extensões de unidade de dados de alguns exemplos, o que economiza espaço e reduz os requisitos de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="c14f5-124">With dynamic data unit extensions, you can omit data unit extensions from some samples, which saves space and reduces bandwidth requirements.</span></span> <span data-ttu-id="c14f5-125">No entanto, se as extensões de unidade de dados forem de tamanho variável, o objeto de leitura não poderá verificar os dados de extensão recebidos em relação a um tamanho estático.</span><span class="sxs-lookup"><span data-stu-id="c14f5-125">However, if data unit extensions are of variable size, the reading object cannot verify the received extension data against a static size.</span></span> <span data-ttu-id="c14f5-126">Você deve verificar se os dados de extensão recebidos são válidos e não há distorção mal-intencionada do fluxo de bits.</span><span class="sxs-lookup"><span data-stu-id="c14f5-126">You must verify that the extension data that you receive is valid, and not malicious distortion of the bit stream.</span></span>

<span data-ttu-id="c14f5-127">As extensões de unidade de dados individuais devem ser definidas em exemplos usando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="c14f5-127">Individual data unit extensions must be set on samples by using the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="c14f5-128">Para obter mais informações, consulte [definindo extensões de unidade de dados](setting-data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="c14f5-128">For more information, see [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c14f5-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c14f5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c14f5-130">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="c14f5-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




