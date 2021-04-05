---
description: Driver MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Driver MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825499"
---
# <a name="mstape-driver"></a><span data-ttu-id="eae78-103">Driver MSTape</span><span class="sxs-lookup"><span data-stu-id="eae78-103">MSTape Driver</span></span>

<span data-ttu-id="eae78-104">Este tópico aplica-se ao Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="eae78-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="eae78-105">O driver MSTape dá suporte a dispositivos de camcorder D-VHS e MPEG.</span><span class="sxs-lookup"><span data-stu-id="eae78-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="eae78-106">Ele é exposto a aplicativos como o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="eae78-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="eae78-107">Sua funcionalidade é semelhante à do [MSDV](msdv-driver.md), o driver DV Camcorder:</span><span class="sxs-lookup"><span data-stu-id="eae78-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="eae78-108">Ele aparece nas categorias de filtro "fontes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) e "dispositivos de renderização de streaming WDM" (am \_ KSCATEGORY \_ render).</span><span class="sxs-lookup"><span data-stu-id="eae78-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="eae78-109">Um aplicativo pode criar uma instância do filtro usando a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="eae78-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="eae78-110">Ele tem um pino de saída para captura e transporte do dispositivo e um PIN de entrada para transporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae78-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="eae78-111">Somente um PIN pode ser conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="eae78-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="eae78-112">**Tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="eae78-112">**Media Types**</span></span>

<span data-ttu-id="eae78-113">O PIN de entrada dá suporte a um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eae78-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="eae78-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="eae78-114">Major Type</span></span>   | <span data-ttu-id="eae78-115">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="eae78-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="eae78-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="eae78-116">Subtype</span></span>      | <span data-ttu-id="eae78-117">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="eae78-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="eae78-118">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="eae78-118">Sample Size</span></span>  | <span data-ttu-id="eae78-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="eae78-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="eae78-120">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="eae78-120">Format Block</span></span> | [<span data-ttu-id="eae78-121">**\_Stride de transporte MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="eae78-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="eae78-122">O pino de saída dá suporte a dois tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="eae78-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="eae78-123">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="eae78-123">Major Type</span></span>   | <span data-ttu-id="eae78-124">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="eae78-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="eae78-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="eae78-125">Subtype</span></span>      | <span data-ttu-id="eae78-126">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="eae78-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="eae78-127">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="eae78-127">Sample Size</span></span>  | <span data-ttu-id="eae78-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="eae78-128">192 x 256</span></span>                              |
| <span data-ttu-id="eae78-129">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="eae78-129">Format Block</span></span> | <span data-ttu-id="eae78-130">\_Stride de transporte MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="eae78-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="eae78-131">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="eae78-131">Major Type</span></span>   | <span data-ttu-id="eae78-132">Fluxo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="eae78-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="eae78-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="eae78-133">Subtype</span></span>      | <span data-ttu-id="eae78-134">\_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="eae78-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="eae78-135">Tamanho da Amostra</span><span class="sxs-lookup"><span data-stu-id="eae78-135">Sample Size</span></span>  | <span data-ttu-id="eae78-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="eae78-136">188 x 256</span></span>                              |
| <span data-ttu-id="eae78-137">Bloco de formato</span><span class="sxs-lookup"><span data-stu-id="eae78-137">Format Block</span></span> | <span data-ttu-id="eae78-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="eae78-138">**NULL**</span></span>                               |



 

<span data-ttu-id="eae78-139">**Informações do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="eae78-139">**Device Information**</span></span>

<span data-ttu-id="eae78-140">O driver lê dinamicamente as informações da ROM de configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae78-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="eae78-141">O aplicativo pode recuperar essas informações ligando o moniker do dispositivo a um recipiente de propriedades e chamando o método **IPropertyBag:: Read** .</span><span class="sxs-lookup"><span data-stu-id="eae78-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="eae78-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="eae78-142">Property</span></span>            | <span data-ttu-id="eae78-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="eae78-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="eae78-144">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="eae78-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="eae78-145">UniqueID \_ baixo</span><span class="sxs-lookup"><span data-stu-id="eae78-145">UniqueID\_Low</span></span>       | <span data-ttu-id="eae78-146">ID exclusiva do dispositivo ( **DWORD** insuficiente).</span><span class="sxs-lookup"><span data-stu-id="eae78-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="eae78-147">**Long** (VT \_ i4)</span><span class="sxs-lookup"><span data-stu-id="eae78-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="eae78-148">UniqueID \_ alto</span><span class="sxs-lookup"><span data-stu-id="eae78-148">UniqueID\_High</span></span>      | <span data-ttu-id="eae78-149">ID exclusiva do dispositivo (alta **DWORD**)</span><span class="sxs-lookup"><span data-stu-id="eae78-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="eae78-150">**longo**</span><span class="sxs-lookup"><span data-stu-id="eae78-150">**long**</span></span>            |
| <span data-ttu-id="eae78-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="eae78-151">VendorID</span></span>            | <span data-ttu-id="eae78-152">ID do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="eae78-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="eae78-153">**longo**</span><span class="sxs-lookup"><span data-stu-id="eae78-153">**long**</span></span>            |
| <span data-ttu-id="eae78-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="eae78-154">ModelID</span></span>             | <span data-ttu-id="eae78-155">ID do modelo.</span><span class="sxs-lookup"><span data-stu-id="eae78-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="eae78-156">**longo**</span><span class="sxs-lookup"><span data-stu-id="eae78-156">**long**</span></span>            |
| <span data-ttu-id="eae78-157">VendorText</span><span class="sxs-lookup"><span data-stu-id="eae78-157">VendorText</span></span>          | <span data-ttu-id="eae78-158">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="eae78-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="eae78-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="eae78-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="eae78-160">ModelText</span><span class="sxs-lookup"><span data-stu-id="eae78-160">ModelText</span></span>           | <span data-ttu-id="eae78-161">Nome do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae78-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="eae78-162">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eae78-162">**BSTR**</span></span>            |
| <span data-ttu-id="eae78-163">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="eae78-163">UnitModelText</span></span>       | <span data-ttu-id="eae78-164">Nome do modelo de unidade; pode ser o mesmo que ModelText.</span><span class="sxs-lookup"><span data-stu-id="eae78-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="eae78-165">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eae78-165">**BSTR**</span></span>            |
| <span data-ttu-id="eae78-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="eae78-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="eae78-167">carga de oPCR (controle de plugue de saída).</span><span class="sxs-lookup"><span data-stu-id="eae78-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="eae78-168">Exemplo: 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="eae78-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="eae78-169">**longo**</span><span class="sxs-lookup"><span data-stu-id="eae78-169">**long**</span></span>            |
| <span data-ttu-id="eae78-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="eae78-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="eae78-171">taxa de dados de oPCR.</span><span class="sxs-lookup"><span data-stu-id="eae78-171">oPCR data rate.</span></span> <span data-ttu-id="eae78-172">Exemplos: 0 (S100), 1 (S200) ou 2 (s400).</span><span class="sxs-lookup"><span data-stu-id="eae78-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="eae78-173">**longo**</span><span class="sxs-lookup"><span data-stu-id="eae78-173">**long**</span></span>            |
| <span data-ttu-id="eae78-174">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="eae78-174">DeviceClassGUID</span></span>     | <span data-ttu-id="eae78-175">GUID que identifica o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae78-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="eae78-176">Para MSTape, esse valor é `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="eae78-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="eae78-177">Esse GUID é definido como MSTapeDeviceGUID no arquivo de cabeçalho Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="eae78-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="eae78-178">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eae78-178">**BSTR**</span></span>            |
| <span data-ttu-id="eae78-179">Description</span><span class="sxs-lookup"><span data-stu-id="eae78-179">Description</span></span>         | <span data-ttu-id="eae78-180">Uma descrição do dispositivo, extraída do arquivo INF.</span><span class="sxs-lookup"><span data-stu-id="eae78-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="eae78-181">Essa cadeia de caracteres geralmente contém o nome da marca do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eae78-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="eae78-182">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="eae78-182">**BSTR**</span></span>            |



 

<span data-ttu-id="eae78-183">A ID do dispositivo é um inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="eae78-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="eae78-184">O **DWORD** baixo é armazenado na Propriedade UniqueId \_ Low e o **DWORD** alto é armazenado na \_ Propriedade alta UniqueId.</span><span class="sxs-lookup"><span data-stu-id="eae78-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="eae78-185">Para obter mais informações sobre monikers de dispositivo, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="eae78-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eae78-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eae78-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eae78-187">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="eae78-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="eae78-188">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="eae78-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



