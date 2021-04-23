---
description: Driver MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Driver MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909394"
---
# <a name="mstape-driver"></a><span data-ttu-id="885cb-103">Driver MSTape</span><span class="sxs-lookup"><span data-stu-id="885cb-103">MSTape Driver</span></span>

<span data-ttu-id="885cb-104">Este tópico aplica-se ao Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="885cb-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="885cb-105">O driver MSTape dá suporte a dispositivos de camcorder D-VHS e MPEG.</span><span class="sxs-lookup"><span data-stu-id="885cb-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="885cb-106">Ele é exposto a aplicativos como o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="885cb-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="885cb-107">Sua funcionalidade é semelhante à do [MSDV](msdv-driver.md), o driver DV Camcorder:</span><span class="sxs-lookup"><span data-stu-id="885cb-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="885cb-108">Ele aparece nas categorias de filtro "fontes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) e "dispositivos de renderização de streaming WDM" (am \_ KSCATEGORY \_ render).</span><span class="sxs-lookup"><span data-stu-id="885cb-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="885cb-109">Um aplicativo pode criar uma instância do filtro usando a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="885cb-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="885cb-110">Ele tem um pino de saída para captura e transporte do dispositivo e um PIN de entrada para transporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="885cb-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="885cb-111">Somente um PIN pode ser conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="885cb-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="885cb-112">**Tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="885cb-112">**Media Types**</span></span>

<span data-ttu-id="885cb-113">O PIN de entrada dá suporte a um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="885cb-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="885cb-114">Label</span><span class="sxs-lookup"><span data-stu-id="885cb-114">Label</span></span> | <span data-ttu-id="885cb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="885cb-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="885cb-116">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="885cb-116">Major Type</span></span>   | <span data-ttu-id="885cb-117">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="885cb-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="885cb-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="885cb-118">Subtype</span></span>      | <span data-ttu-id="885cb-119">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="885cb-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="885cb-120">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="885cb-120">Sample Size</span></span>  | <span data-ttu-id="885cb-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="885cb-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="885cb-122">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="885cb-122">Format Block</span></span> | [<span data-ttu-id="885cb-123">**\_Stride de transporte MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="885cb-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="885cb-124">O pino de saída dá suporte a dois tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="885cb-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="885cb-125">Label</span><span class="sxs-lookup"><span data-stu-id="885cb-125">Label</span></span> | <span data-ttu-id="885cb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="885cb-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="885cb-127">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="885cb-127">Major Type</span></span>   | <span data-ttu-id="885cb-128">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="885cb-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="885cb-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="885cb-129">Subtype</span></span>      | <span data-ttu-id="885cb-130">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="885cb-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="885cb-131">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="885cb-131">Sample Size</span></span>  | <span data-ttu-id="885cb-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="885cb-132">192 x 256</span></span>                              |
| <span data-ttu-id="885cb-133">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="885cb-133">Format Block</span></span> | <span data-ttu-id="885cb-134">\_Stride de transporte MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="885cb-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="885cb-135">Label</span><span class="sxs-lookup"><span data-stu-id="885cb-135">Label</span></span> | <span data-ttu-id="885cb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="885cb-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="885cb-137">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="885cb-137">Major Type</span></span>   | <span data-ttu-id="885cb-138">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="885cb-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="885cb-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="885cb-139">Subtype</span></span>      | <span data-ttu-id="885cb-140">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="885cb-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="885cb-141">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="885cb-141">Sample Size</span></span>  | <span data-ttu-id="885cb-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="885cb-142">188 x 256</span></span>                              |
| <span data-ttu-id="885cb-143">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="885cb-143">Format Block</span></span> | <span data-ttu-id="885cb-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="885cb-144">**NULL**</span></span>                               |



 

<span data-ttu-id="885cb-145">**Informações do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="885cb-145">**Device Information**</span></span>

<span data-ttu-id="885cb-146">O driver lê dinamicamente as informações da ROM de configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="885cb-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="885cb-147">O aplicativo pode recuperar essas informações ligando o moniker do dispositivo a um recipiente de propriedades e chamando o método **IPropertyBag:: Read** .</span><span class="sxs-lookup"><span data-stu-id="885cb-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="885cb-148">Propriedade</span><span class="sxs-lookup"><span data-stu-id="885cb-148">Property</span></span>            | <span data-ttu-id="885cb-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="885cb-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="885cb-150">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="885cb-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="885cb-151">UniqueID \_ baixo</span><span class="sxs-lookup"><span data-stu-id="885cb-151">UniqueID\_Low</span></span>       | <span data-ttu-id="885cb-152">ID exclusiva do dispositivo ( **DWORD** insuficiente).</span><span class="sxs-lookup"><span data-stu-id="885cb-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="885cb-153">**Long** (VT \_ i4)</span><span class="sxs-lookup"><span data-stu-id="885cb-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="885cb-154">UniqueID \_ alto</span><span class="sxs-lookup"><span data-stu-id="885cb-154">UniqueID\_High</span></span>      | <span data-ttu-id="885cb-155">ID exclusiva do dispositivo (alta **DWORD**)</span><span class="sxs-lookup"><span data-stu-id="885cb-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="885cb-156">**longo**</span><span class="sxs-lookup"><span data-stu-id="885cb-156">**long**</span></span>            |
| <span data-ttu-id="885cb-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="885cb-157">VendorID</span></span>            | <span data-ttu-id="885cb-158">ID do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="885cb-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="885cb-159">**longo**</span><span class="sxs-lookup"><span data-stu-id="885cb-159">**long**</span></span>            |
| <span data-ttu-id="885cb-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="885cb-160">ModelID</span></span>             | <span data-ttu-id="885cb-161">ID do modelo.</span><span class="sxs-lookup"><span data-stu-id="885cb-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="885cb-162">**longo**</span><span class="sxs-lookup"><span data-stu-id="885cb-162">**long**</span></span>            |
| <span data-ttu-id="885cb-163">VendorText</span><span class="sxs-lookup"><span data-stu-id="885cb-163">VendorText</span></span>          | <span data-ttu-id="885cb-164">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="885cb-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="885cb-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="885cb-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="885cb-166">ModelText</span><span class="sxs-lookup"><span data-stu-id="885cb-166">ModelText</span></span>           | <span data-ttu-id="885cb-167">Nome do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="885cb-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="885cb-168">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="885cb-168">**BSTR**</span></span>            |
| <span data-ttu-id="885cb-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="885cb-169">UnitModelText</span></span>       | <span data-ttu-id="885cb-170">Nome do modelo de unidade; pode ser o mesmo que ModelText.</span><span class="sxs-lookup"><span data-stu-id="885cb-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="885cb-171">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="885cb-171">**BSTR**</span></span>            |
| <span data-ttu-id="885cb-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="885cb-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="885cb-173">carga de oPCR (controle de plugue de saída).</span><span class="sxs-lookup"><span data-stu-id="885cb-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="885cb-174">Exemplo: 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="885cb-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="885cb-175">**longo**</span><span class="sxs-lookup"><span data-stu-id="885cb-175">**long**</span></span>            |
| <span data-ttu-id="885cb-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="885cb-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="885cb-177">taxa de dados de oPCR.</span><span class="sxs-lookup"><span data-stu-id="885cb-177">oPCR data rate.</span></span> <span data-ttu-id="885cb-178">Exemplos: 0 (S100), 1 (S200) ou 2 (s400).</span><span class="sxs-lookup"><span data-stu-id="885cb-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="885cb-179">**longo**</span><span class="sxs-lookup"><span data-stu-id="885cb-179">**long**</span></span>            |
| <span data-ttu-id="885cb-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="885cb-180">DeviceClassGUID</span></span>     | <span data-ttu-id="885cb-181">GUID que identifica o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="885cb-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="885cb-182">Para MSTape, esse valor é `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="885cb-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="885cb-183">Esse GUID é definido como MSTapeDeviceGUID no arquivo de cabeçalho Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="885cb-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="885cb-184">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="885cb-184">**BSTR**</span></span>            |
| <span data-ttu-id="885cb-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="885cb-185">Description</span></span>         | <span data-ttu-id="885cb-186">Uma descrição do dispositivo, extraída do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="885cb-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="885cb-187">Essa cadeia de caracteres geralmente contém o nome da marca do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="885cb-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="885cb-188">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="885cb-188">**BSTR**</span></span>            |



 

<span data-ttu-id="885cb-189">A ID do dispositivo é um inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="885cb-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="885cb-190">O **DWORD** baixo é armazenado na Propriedade UniqueId \_ Low e o **DWORD** alto é armazenado na \_ Propriedade alta UniqueId.</span><span class="sxs-lookup"><span data-stu-id="885cb-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="885cb-191">Para obter mais informações sobre monikers de dispositivo, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="885cb-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="885cb-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="885cb-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885cb-193">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="885cb-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="885cb-194">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="885cb-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



