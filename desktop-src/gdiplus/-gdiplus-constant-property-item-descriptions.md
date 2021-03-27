---
description: A lista a seguir fornece descrições dos itens de propriedade com suporte no Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descrições de item de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636118"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="9e8ee-103">Descrições de item de propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-103">Property Item Descriptions</span></span>

<span data-ttu-id="9e8ee-104">A lista a seguir fornece descrições dos itens de propriedade com suporte no Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="9e8ee-105">As descrições são breves e gerais para que se apliquem a uma variedade de formatos de arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="9e8ee-106">Para obter uma descrição detalhada de como um item de propriedade é usado por um determinado formato de arquivo, consulte a especificação para esse formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="9e8ee-107">Para obter links para várias especificações de arquivo e outros documentos que descrevem metadados em detalhes, consulte [especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="9e8ee-108">O formato EXIF (exchangável Image File) é um padrão JEIDA (Associação de desenvolvimento do setor eletrônico) do Japão, revisado em junho de 1998 como a versão 2,1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="9e8ee-109">Partes da especificação EXIF são usadas com a permissão de JEIDA.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="9e8ee-110">PropertyTagGpsVer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="9e8ee-111">Versão da IFD GPS (Global Positioning Systems), fornecida como 2.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="9e8ee-112">Essa marca é obrigatória quando a marca PropertyTagGpsIFD está presente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="9e8ee-113">Quando a versão for 2.0.0.0, o valor da marca será 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="9e8ee-114">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-114">Property info</span></span> | <span data-ttu-id="9e8ee-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-116">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-116">Tag</span></span>   | <span data-ttu-id="9e8ee-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="9e8ee-117">0x0000</span></span>              |
| <span data-ttu-id="9e8ee-118">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-118">Type</span></span>  | <span data-ttu-id="9e8ee-119">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-120">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-120">Count</span></span> | <span data-ttu-id="9e8ee-121">4</span><span class="sxs-lookup"><span data-stu-id="9e8ee-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="9e8ee-122">PropertyTagGpsLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="9e8ee-123">Cadeia de caracteres terminada em nulo que especifica se a latitude é norte ou Sul.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="9e8ee-124">`N` Especifica a latitude do Norte e `S` especifica a latitude do Sul.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="9e8ee-125">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-125">Property info</span></span> | <span data-ttu-id="9e8ee-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-127">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-127">Tag</span></span>   | <span data-ttu-id="9e8ee-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="9e8ee-128">0x0001</span></span>                                     |
| <span data-ttu-id="9e8ee-129">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-129">Type</span></span>  | <span data-ttu-id="9e8ee-130">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-131">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-131">Count</span></span> | <span data-ttu-id="9e8ee-132">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="9e8ee-133">PropertyTagGpsLatitude</span><span class="sxs-lookup"><span data-stu-id="9e8ee-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="9e8ee-134">Latitude.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-134">Latitude.</span></span> <span data-ttu-id="9e8ee-135">A latitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="9e8ee-136">Quando graus, minutos e segundos são expressos, o formato é dd/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="9e8ee-137">Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é dd/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="9e8ee-138">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-138">Property info</span></span> | <span data-ttu-id="9e8ee-139">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-140">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-140">Tag</span></span>   | <span data-ttu-id="9e8ee-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="9e8ee-141">0x0002</span></span>                  |
| <span data-ttu-id="9e8ee-142">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-142">Type</span></span>  | <span data-ttu-id="9e8ee-143">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-144">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-144">Count</span></span> | <span data-ttu-id="9e8ee-145">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="9e8ee-146">PropertyTagGpsLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="9e8ee-147">Cadeia de caracteres terminada em nulo que especifica se a longitude é a longitude Oriental ou oeste.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="9e8ee-148">`E` Especifica a longitude Oriental e `W` especifica a longitude ocidental.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="9e8ee-149">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-149">Property info</span></span> | <span data-ttu-id="9e8ee-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-151">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-151">Tag</span></span>   | <span data-ttu-id="9e8ee-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="9e8ee-152">0x0003</span></span>                                     |
| <span data-ttu-id="9e8ee-153">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-153">Type</span></span>  | <span data-ttu-id="9e8ee-154">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-155">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-155">Count</span></span> | <span data-ttu-id="9e8ee-156">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="9e8ee-157">PropertyTagGpsLongitude</span><span class="sxs-lookup"><span data-stu-id="9e8ee-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="9e8ee-158">Longitude.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-158">Longitude.</span></span> <span data-ttu-id="9e8ee-159">A longitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="9e8ee-160">Quando graus, minutos e segundos são expressos, o formato é DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="9e8ee-161">Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="9e8ee-162">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-162">Property info</span></span> | <span data-ttu-id="9e8ee-163">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-164">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-164">Tag</span></span>   | <span data-ttu-id="9e8ee-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="9e8ee-165">0x0004</span></span>                  |
| <span data-ttu-id="9e8ee-166">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-166">Type</span></span>  | <span data-ttu-id="9e8ee-167">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-168">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-168">Count</span></span> | <span data-ttu-id="9e8ee-169">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="9e8ee-170">PropertyTagGpsAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="9e8ee-171">Altitude de referência, em metros.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="9e8ee-172">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-172">Property info</span></span> | <span data-ttu-id="9e8ee-173">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-174">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-174">Tag</span></span>   | <span data-ttu-id="9e8ee-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="9e8ee-175">0x0005</span></span>              |
| <span data-ttu-id="9e8ee-176">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-176">Type</span></span>  | <span data-ttu-id="9e8ee-177">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-178">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-178">Count</span></span> | <span data-ttu-id="9e8ee-179">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="9e8ee-180">PropertyTagGpsAltitude</span><span class="sxs-lookup"><span data-stu-id="9e8ee-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="9e8ee-181">Altitude, em metros, com base na altitude de referência especificada por PropertyTagGpsAltitudeRef.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="9e8ee-182">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-182">Property info</span></span> | <span data-ttu-id="9e8ee-183">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-184">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-184">Tag</span></span>   | <span data-ttu-id="9e8ee-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="9e8ee-185">0x0006</span></span>                  |
| <span data-ttu-id="9e8ee-186">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-186">Type</span></span>  | <span data-ttu-id="9e8ee-187">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-188">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-188">Count</span></span> | <span data-ttu-id="9e8ee-189">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="9e8ee-190">PropertyTagGpsGpsTime</span><span class="sxs-lookup"><span data-stu-id="9e8ee-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="9e8ee-191">Tempo como UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9e8ee-192">O valor é expresso como três números racionales que fornecem a hora, minuto e segundo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="9e8ee-193">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-193">Property info</span></span> | <span data-ttu-id="9e8ee-194">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-195">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-195">Tag</span></span>   | <span data-ttu-id="9e8ee-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="9e8ee-196">0x0007</span></span>                  |
| <span data-ttu-id="9e8ee-197">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-197">Type</span></span>  | <span data-ttu-id="9e8ee-198">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-199">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-199">Count</span></span> | <span data-ttu-id="9e8ee-200">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="9e8ee-201">PropertyTagGpsGpsSatellites</span><span class="sxs-lookup"><span data-stu-id="9e8ee-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="9e8ee-202">Cadeia de caracteres terminada em nulo que especifica os satélites de GPS usados para medições.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="9e8ee-203">Essa marca pode ser usada para especificar o número de ID, o ângulo de elevação, Azimuth, SNR e outras informações sobre cada satélite.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="9e8ee-204">O formato não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-204">The format is not specified.</span></span> <span data-ttu-id="9e8ee-205">Se o receptor GPS for incapaz de fazer medições, o valor da marca deverá ser definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="9e8ee-206">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-206">Property info</span></span> | <span data-ttu-id="9e8ee-207">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-208">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-208">Tag</span></span>   | <span data-ttu-id="9e8ee-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="9e8ee-209">0x0008</span></span>                                             |
| <span data-ttu-id="9e8ee-210">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-210">Type</span></span>  | <span data-ttu-id="9e8ee-211">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-212">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-212">Count</span></span> | <span data-ttu-id="9e8ee-213">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="9e8ee-214">PropertyTagGpsGpsStatus</span><span class="sxs-lookup"><span data-stu-id="9e8ee-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="9e8ee-215">Cadeia de caracteres terminada em nulo que especifica o status do receptor GPS quando a imagem é registrada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="9e8ee-216">`A` significa que a medição está em andamento e `V` significa que a medição é interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="9e8ee-217">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-217">Property info</span></span> | <span data-ttu-id="9e8ee-218">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-219">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-219">Tag</span></span>   | <span data-ttu-id="9e8ee-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="9e8ee-220">0x0009</span></span>                                     |
| <span data-ttu-id="9e8ee-221">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-221">Type</span></span>  | <span data-ttu-id="9e8ee-222">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-223">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-223">Count</span></span> | <span data-ttu-id="9e8ee-224">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="9e8ee-225">PropertyTagGpsGpsMeasureMode</span><span class="sxs-lookup"><span data-stu-id="9e8ee-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="9e8ee-226">Cadeia de caracteres terminada em nulo que especifica o modo de medição GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="9e8ee-227">`2` Especifica a medida de 2-D e `3` especifica a medida 3D.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="9e8ee-228">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-228">Property info</span></span> | <span data-ttu-id="9e8ee-229">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-230">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-230">Tag</span></span>   | <span data-ttu-id="9e8ee-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-231">0x000A</span></span>                                     |
| <span data-ttu-id="9e8ee-232">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-232">Type</span></span>  | <span data-ttu-id="9e8ee-233">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-234">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-234">Count</span></span> | <span data-ttu-id="9e8ee-235">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="9e8ee-236">PropertyTagGpsGpsDop</span><span class="sxs-lookup"><span data-stu-id="9e8ee-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="9e8ee-237">DOP GPS (grau de precisão de dados).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="9e8ee-238">Um valor de HDOP é gravado durante a medição de 2D e um valor de PDOP é gravado durante a medição 3D.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="9e8ee-239">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-239">Property info</span></span> | <span data-ttu-id="9e8ee-240">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-241">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-241">Tag</span></span>   | <span data-ttu-id="9e8ee-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-242">0x000B</span></span>                  |
| <span data-ttu-id="9e8ee-243">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-243">Type</span></span>  | <span data-ttu-id="9e8ee-244">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-245">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-245">Count</span></span> | <span data-ttu-id="9e8ee-246">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="9e8ee-247">PropertyTagGpsSpeedRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="9e8ee-248">Cadeia de caracteres terminada em nulo que especifica a unidade usada para expressar a velocidade do movimento do receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="9e8ee-249">`K`, `M` e `N` representam quilômetros por hora, milhas por hora e nós respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="9e8ee-250">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-250">Property info</span></span> | <span data-ttu-id="9e8ee-251">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-252">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-252">Tag</span></span>   | <span data-ttu-id="9e8ee-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-253">0x000C</span></span>                                     |
| <span data-ttu-id="9e8ee-254">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-254">Type</span></span>  | <span data-ttu-id="9e8ee-255">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-256">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-256">Count</span></span> | <span data-ttu-id="9e8ee-257">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="9e8ee-258">PropertyTagGpsSpeed</span><span class="sxs-lookup"><span data-stu-id="9e8ee-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="9e8ee-259">Velocidade do movimento do receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="9e8ee-260">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-260">Property info</span></span> | <span data-ttu-id="9e8ee-261">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-262">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-262">Tag</span></span>   | <span data-ttu-id="9e8ee-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-263">0x000D</span></span>                  |
| <span data-ttu-id="9e8ee-264">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-264">Type</span></span>  | <span data-ttu-id="9e8ee-265">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-266">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-266">Count</span></span> | <span data-ttu-id="9e8ee-267">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="9e8ee-268">PropertyTagGpsTrackRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="9e8ee-269">Cadeia de caracteres terminada em nulo que especifica a referência para dar a direção do movimento do receptor de GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="9e8ee-270">`T` Especifica a direção true e `M` especifica a direção magnética.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="9e8ee-271">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-271">Property info</span></span> | <span data-ttu-id="9e8ee-272">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-273">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-273">Tag</span></span>   | <span data-ttu-id="9e8ee-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-274">0x000E</span></span>                                     |
| <span data-ttu-id="9e8ee-275">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-275">Type</span></span>  | <span data-ttu-id="9e8ee-276">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-277">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-277">Count</span></span> | <span data-ttu-id="9e8ee-278">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="9e8ee-279">PropertyTagGpsTrack</span><span class="sxs-lookup"><span data-stu-id="9e8ee-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="9e8ee-280">Direção da movimentação do receptor de GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="9e8ee-281">O intervalo de valores é de 0, 0 a 359,99.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="9e8ee-282">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-282">Property info</span></span> | <span data-ttu-id="9e8ee-283">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-284">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-284">Tag</span></span>   | <span data-ttu-id="9e8ee-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-285">0x000F</span></span>                  |
| <span data-ttu-id="9e8ee-286">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-286">Type</span></span>  | <span data-ttu-id="9e8ee-287">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-288">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-288">Count</span></span> | <span data-ttu-id="9e8ee-289">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="9e8ee-290">PropertyTagGpsImgDirRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="9e8ee-291">Cadeia de caracteres terminada em nulo que especifica a referência para a direção da imagem quando ela é capturada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="9e8ee-292">`T` Especifica a direção true e `M` especifica a direção magnética.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="9e8ee-293">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-293">Property info</span></span> | <span data-ttu-id="9e8ee-294">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-295">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-295">Tag</span></span>   | <span data-ttu-id="9e8ee-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="9e8ee-296">0x0010</span></span>                                     |
| <span data-ttu-id="9e8ee-297">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-297">Type</span></span>  | <span data-ttu-id="9e8ee-298">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-299">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-299">Count</span></span> | <span data-ttu-id="9e8ee-300">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="9e8ee-301">PropertyTagGpsImgDir</span><span class="sxs-lookup"><span data-stu-id="9e8ee-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="9e8ee-302">Direção da imagem quando ela foi capturada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="9e8ee-303">O intervalo de valores é de 0, 0 a 359,99.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="9e8ee-304">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-304">Property info</span></span> | <span data-ttu-id="9e8ee-305">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-306">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-306">Tag</span></span>   | <span data-ttu-id="9e8ee-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="9e8ee-307">0x0011</span></span>                  |
| <span data-ttu-id="9e8ee-308">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-308">Type</span></span>  | <span data-ttu-id="9e8ee-309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-310">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-310">Count</span></span> | <span data-ttu-id="9e8ee-311">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="9e8ee-312">PropertyTagGpsMapDatum</span><span class="sxs-lookup"><span data-stu-id="9e8ee-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="9e8ee-313">Cadeia de caracteres terminada em nulo que especifica dados de pesquisa geodésico usados pelo receptor GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="9e8ee-314">Se os dados da pesquisa estiverem restritos ao Japão, o valor dessa marca será `TOKYO` ou `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="9e8ee-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="9e8ee-315">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-315">Property info</span></span> | <span data-ttu-id="9e8ee-316">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-317">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-317">Tag</span></span>   | <span data-ttu-id="9e8ee-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="9e8ee-318">0x0012</span></span>                                             |
| <span data-ttu-id="9e8ee-319">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-319">Type</span></span>  | <span data-ttu-id="9e8ee-320">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-321">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-321">Count</span></span> | <span data-ttu-id="9e8ee-322">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="9e8ee-323">PropertyTagGpsDestLatRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="9e8ee-324">Cadeia de caracteres terminada em nulo que especifica se a latitude do ponto de destino é norte ou sul da latitude.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="9e8ee-325">`N` Especifica a latitude do Norte e `S` especifica a latitude do Sul.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="9e8ee-326">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-326">Property info</span></span> | <span data-ttu-id="9e8ee-327">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-328">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-328">Tag</span></span>   | <span data-ttu-id="9e8ee-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="9e8ee-329">0x0013</span></span>                                     |
| <span data-ttu-id="9e8ee-330">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-330">Type</span></span>  | <span data-ttu-id="9e8ee-331">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-332">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-332">Count</span></span> | <span data-ttu-id="9e8ee-333">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="9e8ee-334">PropertyTagGpsDestLat</span><span class="sxs-lookup"><span data-stu-id="9e8ee-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="9e8ee-335">Latitude do ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-335">Latitude of the destination point.</span></span> <span data-ttu-id="9e8ee-336">A latitude é expressa como três valores racionalizados fornecendo os graus, minutos e segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="9e8ee-337">Quando graus, minutos e segundos são expressos, o formato é dd/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="9e8ee-338">Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é dd/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="9e8ee-339">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-339">Property info</span></span> | <span data-ttu-id="9e8ee-340">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-341">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-341">Tag</span></span>   | <span data-ttu-id="9e8ee-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="9e8ee-342">0x0014</span></span>                  |
| <span data-ttu-id="9e8ee-343">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-343">Type</span></span>  | <span data-ttu-id="9e8ee-344">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-345">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-345">Count</span></span> | <span data-ttu-id="9e8ee-346">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="9e8ee-347">PropertyTagGpsDestLongRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="9e8ee-348">Cadeia de caracteres terminada em nulo que especifica se a longitude do ponto de destino é a longitude Oriental ou oeste.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="9e8ee-349">`E` Especifica a longitude Oriental e `W` especifica a longitude ocidental.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="9e8ee-350">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-350">Property info</span></span> | <span data-ttu-id="9e8ee-351">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-352">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-352">Tag</span></span>   | <span data-ttu-id="9e8ee-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="9e8ee-353">0x0015</span></span>                                     |
| <span data-ttu-id="9e8ee-354">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-354">Type</span></span>  | <span data-ttu-id="9e8ee-355">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-356">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-356">Count</span></span> | <span data-ttu-id="9e8ee-357">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="9e8ee-358">PropertyTagGpsDestLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="9e8ee-359">Longitude do ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-359">Longitude of the destination point.</span></span> <span data-ttu-id="9e8ee-360">A longitude é expressa como três valores racionalizados fornecendo os graus, os minutos e os segundos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="9e8ee-361">Quando graus, minutos e segundos são expressos, o formato é DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="9e8ee-362">Quando os graus e minutos são usados e, por exemplo, frações de minutos são dadas até duas casas decimais, o formato é DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="9e8ee-363">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-363">Property info</span></span> | <span data-ttu-id="9e8ee-364">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-365">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-365">Tag</span></span>   | <span data-ttu-id="9e8ee-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="9e8ee-366">0x0016</span></span>                  |
| <span data-ttu-id="9e8ee-367">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-367">Type</span></span>  | <span data-ttu-id="9e8ee-368">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-369">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-369">Count</span></span> | <span data-ttu-id="9e8ee-370">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="9e8ee-371">PropertyTagGpsDestBearRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="9e8ee-372">Cadeia de caracteres terminada em nulo que especifica a referência usada para dar a passagem ao ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="9e8ee-373">`T` Especifica a direção true e `M` especifica a direção magnética.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="9e8ee-374">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-374">Property info</span></span> | <span data-ttu-id="9e8ee-375">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-376">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-376">Tag</span></span>   | <span data-ttu-id="9e8ee-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="9e8ee-377">0x0017</span></span>                                     |
| <span data-ttu-id="9e8ee-378">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-378">Type</span></span>  | <span data-ttu-id="9e8ee-379">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-380">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-380">Count</span></span> | <span data-ttu-id="9e8ee-381">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="9e8ee-382">PropertyTagGpsDestBear</span><span class="sxs-lookup"><span data-stu-id="9e8ee-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="9e8ee-383">Enrumo ao ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-383">Bearing to the destination point.</span></span> <span data-ttu-id="9e8ee-384">O intervalo de valores é de 0, 0 a 359,99.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="9e8ee-385">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-385">Property info</span></span> | <span data-ttu-id="9e8ee-386">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-387">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-387">Tag</span></span>   | <span data-ttu-id="9e8ee-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="9e8ee-388">0x0018</span></span>                  |
| <span data-ttu-id="9e8ee-389">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-389">Type</span></span>  | <span data-ttu-id="9e8ee-390">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-391">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-391">Count</span></span> | <span data-ttu-id="9e8ee-392">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="9e8ee-393">PropertyTagGpsDestDistRef</span><span class="sxs-lookup"><span data-stu-id="9e8ee-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="9e8ee-394">Cadeia de caracteres terminada em nulo que especifica a unidade usada para expressar a distância para o ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="9e8ee-395">K, M e N representam quilômetros, milhas e nós, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="9e8ee-396">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-396">Property info</span></span> | <span data-ttu-id="9e8ee-397">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="9e8ee-398">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-398">Tag</span></span>   | <span data-ttu-id="9e8ee-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="9e8ee-399">0x0019</span></span>                                     |
| <span data-ttu-id="9e8ee-400">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-400">Type</span></span>  | <span data-ttu-id="9e8ee-401">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="9e8ee-402">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-402">Count</span></span> | <span data-ttu-id="9e8ee-403">2 (um caractere mais o terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="9e8ee-404">PropertyTagGpsDestDist</span><span class="sxs-lookup"><span data-stu-id="9e8ee-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="9e8ee-405">Distância para o ponto de destino.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-405">Distance to the destination point.</span></span>



| <span data-ttu-id="9e8ee-406">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-406">Property info</span></span> | <span data-ttu-id="9e8ee-407">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-408">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-408">Tag</span></span>   | <span data-ttu-id="9e8ee-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-409">0x001A</span></span>                  |
| <span data-ttu-id="9e8ee-410">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-410">Type</span></span>  | <span data-ttu-id="9e8ee-411">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-412">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-412">Count</span></span> | <span data-ttu-id="9e8ee-413">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="9e8ee-414">PropertyTagNewSubfileType</span><span class="sxs-lookup"><span data-stu-id="9e8ee-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="9e8ee-415">Tipo de dados em um subarquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="9e8ee-416">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-416">Property info</span></span> | <span data-ttu-id="9e8ee-417">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-418">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-418">Tag</span></span>   | <span data-ttu-id="9e8ee-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="9e8ee-419">0x00FE</span></span>              |
| <span data-ttu-id="9e8ee-420">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-420">Type</span></span>  | <span data-ttu-id="9e8ee-421">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-422">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-422">Count</span></span> | <span data-ttu-id="9e8ee-423">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="9e8ee-424">PropertyTagSubfileType</span><span class="sxs-lookup"><span data-stu-id="9e8ee-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="9e8ee-425">Tipo de dados em um subarquivo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="9e8ee-426">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-426">Property info</span></span> | <span data-ttu-id="9e8ee-427">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-428">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-428">Tag</span></span>   | <span data-ttu-id="9e8ee-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="9e8ee-429">0x00FF</span></span>               |
| <span data-ttu-id="9e8ee-430">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-430">Type</span></span>  | <span data-ttu-id="9e8ee-431">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-432">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-432">Count</span></span> | <span data-ttu-id="9e8ee-433">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="9e8ee-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="9e8ee-435">Número de pixels por linha.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-435">Number of pixels per row.</span></span>



| <span data-ttu-id="9e8ee-436">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-436">Property info</span></span> | <span data-ttu-id="9e8ee-437">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-438">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-438">Tag</span></span>   | <span data-ttu-id="9e8ee-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="9e8ee-439">0x0100</span></span>                                      |
| <span data-ttu-id="9e8ee-440">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-440">Type</span></span>  | <span data-ttu-id="9e8ee-441">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-442">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-442">Count</span></span> | <span data-ttu-id="9e8ee-443">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="9e8ee-444">PropertyTagImageHeight</span><span class="sxs-lookup"><span data-stu-id="9e8ee-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="9e8ee-445">Número de linhas de pixel.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-445">Number of pixel rows.</span></span>



| <span data-ttu-id="9e8ee-446">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-446">Property info</span></span> | <span data-ttu-id="9e8ee-447">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-448">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-448">Tag</span></span>   | <span data-ttu-id="9e8ee-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="9e8ee-449">0x0101</span></span>                                      |
| <span data-ttu-id="9e8ee-450">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-450">Type</span></span>  | <span data-ttu-id="9e8ee-451">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-452">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-452">Count</span></span> | <span data-ttu-id="9e8ee-453">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="9e8ee-454">PropertyTagBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="9e8ee-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="9e8ee-455">Número de bits por componente de cor.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-455">Number of bits per color component.</span></span> <span data-ttu-id="9e8ee-456">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-457">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-457">Property info</span></span> | <span data-ttu-id="9e8ee-458">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-459">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-459">Tag</span></span>   | <span data-ttu-id="9e8ee-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="9e8ee-460">0x0102</span></span>                                   |
| <span data-ttu-id="9e8ee-461">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-461">Type</span></span>  | <span data-ttu-id="9e8ee-462">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-463">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-463">Count</span></span> | <span data-ttu-id="9e8ee-464">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="9e8ee-465">PropertyTagCompression</span><span class="sxs-lookup"><span data-stu-id="9e8ee-465">PropertyTagCompression</span></span>

<span data-ttu-id="9e8ee-466">Esquema de compactação usado para os dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="9e8ee-467">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-467">Property info</span></span> | <span data-ttu-id="9e8ee-468">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-469">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-469">Tag</span></span>   | <span data-ttu-id="9e8ee-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="9e8ee-470">0x0103</span></span>               |
| <span data-ttu-id="9e8ee-471">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-471">Type</span></span>  | <span data-ttu-id="9e8ee-472">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-473">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-473">Count</span></span> | <span data-ttu-id="9e8ee-474">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="9e8ee-475">PropertyTagPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="9e8ee-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="9e8ee-476">Como os dados de pixel serão interpretados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="9e8ee-477">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-477">Property info</span></span> | <span data-ttu-id="9e8ee-478">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-479">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-479">Tag</span></span>   | <span data-ttu-id="9e8ee-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="9e8ee-480">0x0106</span></span>               |
| <span data-ttu-id="9e8ee-481">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-481">Type</span></span>  | <span data-ttu-id="9e8ee-482">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-483">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-483">Count</span></span> | <span data-ttu-id="9e8ee-484">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="9e8ee-485">PropertyTagThreshHolding</span><span class="sxs-lookup"><span data-stu-id="9e8ee-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="9e8ee-486">Técnica usada para converter pixels de cinza em pixels pretos e brancos.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="9e8ee-487">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-487">Property info</span></span> | <span data-ttu-id="9e8ee-488">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-489">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-489">Tag</span></span>   | <span data-ttu-id="9e8ee-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="9e8ee-490">0x0107</span></span>               |
| <span data-ttu-id="9e8ee-491">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-491">Type</span></span>  | <span data-ttu-id="9e8ee-492">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-493">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-493">Count</span></span> | <span data-ttu-id="9e8ee-494">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="9e8ee-495">PropertyTagCellWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="9e8ee-496">Largura da matriz de pontilhamento ou de meio-tom.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="9e8ee-497">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-497">Property info</span></span> | <span data-ttu-id="9e8ee-498">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-499">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-499">Tag</span></span>   | <span data-ttu-id="9e8ee-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="9e8ee-500">0x0108</span></span>               |
| <span data-ttu-id="9e8ee-501">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-501">Type</span></span>  | <span data-ttu-id="9e8ee-502">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-503">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-503">Count</span></span> | <span data-ttu-id="9e8ee-504">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="9e8ee-505">PropertyTagCellHeight</span><span class="sxs-lookup"><span data-stu-id="9e8ee-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="9e8ee-506">Altura da matriz de pontilhado ou de meio-tom.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="9e8ee-507">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-507">Property info</span></span> | <span data-ttu-id="9e8ee-508">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-509">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-509">Tag</span></span>   | <span data-ttu-id="9e8ee-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="9e8ee-510">0x0109</span></span>               |
| <span data-ttu-id="9e8ee-511">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-511">Type</span></span>  | <span data-ttu-id="9e8ee-512">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-513">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-513">Count</span></span> | <span data-ttu-id="9e8ee-514">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="9e8ee-515">PropertyTagFillOrder</span><span class="sxs-lookup"><span data-stu-id="9e8ee-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="9e8ee-516">Ordem lógica de bits em um byte.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="9e8ee-517">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-517">Property info</span></span> | <span data-ttu-id="9e8ee-518">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-519">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-519">Tag</span></span>   | <span data-ttu-id="9e8ee-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-520">0x010A</span></span>               |
| <span data-ttu-id="9e8ee-521">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-521">Type</span></span>  | <span data-ttu-id="9e8ee-522">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-523">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-523">Count</span></span> | <span data-ttu-id="9e8ee-524">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="9e8ee-525">PropertyTagDocumentName</span><span class="sxs-lookup"><span data-stu-id="9e8ee-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="9e8ee-526">Cadeia de caracteres terminada em nulo que especifica o nome do documento do qual a imagem foi verificada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="9e8ee-527">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-527">Property info</span></span> | <span data-ttu-id="9e8ee-528">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-529">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-529">Tag</span></span>   | <span data-ttu-id="9e8ee-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-530">0x010D</span></span>                                             |
| <span data-ttu-id="9e8ee-531">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-531">Type</span></span>  | <span data-ttu-id="9e8ee-532">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-533">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-533">Count</span></span> | <span data-ttu-id="9e8ee-534">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="9e8ee-535">PropertyTagImageDescription</span><span class="sxs-lookup"><span data-stu-id="9e8ee-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="9e8ee-536">Cadeia de caracteres terminada em nulo que especifica o título da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="9e8ee-537">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-537">Property info</span></span> | <span data-ttu-id="9e8ee-538">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-539">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-539">Tag</span></span>   | <span data-ttu-id="9e8ee-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-540">0x010E</span></span>                                             |
| <span data-ttu-id="9e8ee-541">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-541">Type</span></span>  | <span data-ttu-id="9e8ee-542">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-543">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-543">Count</span></span> | <span data-ttu-id="9e8ee-544">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="9e8ee-545">PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="9e8ee-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="9e8ee-546">Cadeia de caracteres terminada em nulo que especifica o fabricante do equipamento usado para gravar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="9e8ee-547">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-547">Property info</span></span> | <span data-ttu-id="9e8ee-548">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-549">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-549">Tag</span></span>   | <span data-ttu-id="9e8ee-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-550">0x010F</span></span>                                             |
| <span data-ttu-id="9e8ee-551">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-551">Type</span></span>  | <span data-ttu-id="9e8ee-552">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-553">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-553">Count</span></span> | <span data-ttu-id="9e8ee-554">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="9e8ee-555">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="9e8ee-556">Cadeia de caracteres terminada em nulo que especifica o nome do modelo ou o número do modelo do equipamento usado para gravar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="9e8ee-557">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-557">Property info</span></span> | <span data-ttu-id="9e8ee-558">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-559">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-559">Tag</span></span>   | <span data-ttu-id="9e8ee-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="9e8ee-560">0x0110</span></span>                                             |
| <span data-ttu-id="9e8ee-561">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-561">Type</span></span>  | <span data-ttu-id="9e8ee-562">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-563">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-563">Count</span></span> | <span data-ttu-id="9e8ee-564">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="9e8ee-565">PropertyTagStripOffsets</span><span class="sxs-lookup"><span data-stu-id="9e8ee-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="9e8ee-566">Para cada faixa, o deslocamento de byte dessa faixa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="9e8ee-567">Consulte também [PropertyTagRowsPerStrip](#propertytagrowsperstrip) e [PropertyTagStripBytesCount](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="9e8ee-568">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-568">Property info</span></span> | <span data-ttu-id="9e8ee-569">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-570">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-570">Tag</span></span>   | <span data-ttu-id="9e8ee-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="9e8ee-571">0x0111</span></span>                                      |
| <span data-ttu-id="9e8ee-572">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-572">Type</span></span>  | <span data-ttu-id="9e8ee-573">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-574">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-574">Count</span></span> | <span data-ttu-id="9e8ee-575">Número de faixas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="9e8ee-576">PropertyTagOrientation</span><span class="sxs-lookup"><span data-stu-id="9e8ee-576">PropertyTagOrientation</span></span>

<span data-ttu-id="9e8ee-577">Orientação da imagem exibida em termos de linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="9e8ee-578">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-578">Tag</span></span>

<span data-ttu-id="9e8ee-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="9e8ee-579">0x0112</span></span>

<span data-ttu-id="9e8ee-580">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-580">Type</span></span>

<span data-ttu-id="9e8ee-581">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-582">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-582">Count</span></span>

<span data-ttu-id="9e8ee-583">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-583">1</span></span>

<span data-ttu-id="9e8ee-584">1-a linha 0º está na parte superior da imagem visual e a coluna 0º é a do lado esquerdo do Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="9e8ee-585">2-a linha 0º está na parte superior visual da imagem e a coluna 0º é o lado direito Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="9e8ee-586">3-a linha 0º está na parte inferior Visual da imagem e a coluna 0º é o lado direito Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="9e8ee-587">4-a linha 0º está na parte inferior Visual da imagem e a coluna 0º é o lado esquerdo do Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="9e8ee-588">5-a linha 0º é o lado esquerdo do Visual da imagem e a coluna 0º é a parte superior visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="9e8ee-589">6-a linha 0º é o lado direito Visual da imagem e a coluna 0º é a parte superior visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="9e8ee-590">7-a linha 0º é o lado direito Visual da imagem e a coluna 0º é a parte inferior Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="9e8ee-591">8-a linha 0º é o lado esquerdo do Visual da imagem e a coluna 0º é a parte inferior Visual.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="9e8ee-592">PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="9e8ee-593">Número de componentes de cores por pixel.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="9e8ee-594">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-594">Property info</span></span> | <span data-ttu-id="9e8ee-595">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-596">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-596">Tag</span></span>   | <span data-ttu-id="9e8ee-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="9e8ee-597">0x0115</span></span>               |
| <span data-ttu-id="9e8ee-598">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-598">Type</span></span>  | <span data-ttu-id="9e8ee-599">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-600">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-600">Count</span></span> | <span data-ttu-id="9e8ee-601">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="9e8ee-602">PropertyTagRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="9e8ee-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="9e8ee-603">Número de linhas por faixa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-603">Number of rows per strip.</span></span> <span data-ttu-id="9e8ee-604">Consulte também [PropertyTagStripBytesCount](#propertytagstripbytescount) e [PropertyTagStripOffsets](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="9e8ee-605">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-605">Property info</span></span> | <span data-ttu-id="9e8ee-606">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-607">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-607">Tag</span></span>   | <span data-ttu-id="9e8ee-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="9e8ee-608">0x0116</span></span>                                      |
| <span data-ttu-id="9e8ee-609">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-609">Type</span></span>  | <span data-ttu-id="9e8ee-610">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-611">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-611">Count</span></span> | <span data-ttu-id="9e8ee-612">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="9e8ee-613">PropertyTagStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="9e8ee-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="9e8ee-614">Para cada faixa, o número total de bytes nessa faixa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="9e8ee-615">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-615">Property info</span></span> | <span data-ttu-id="9e8ee-616">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-617">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-617">Tag</span></span>   | <span data-ttu-id="9e8ee-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="9e8ee-618">0x0117</span></span>                                      |
| <span data-ttu-id="9e8ee-619">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-619">Type</span></span>  | <span data-ttu-id="9e8ee-620">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-621">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-621">Count</span></span> | <span data-ttu-id="9e8ee-622">Número de faixas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="9e8ee-623">PropertyTagMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="9e8ee-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="9e8ee-624">Para cada componente de cor, o valor mínimo atribuído a esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="9e8ee-625">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-626">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-626">Property info</span></span> | <span data-ttu-id="9e8ee-627">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-628">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-628">Tag</span></span>   | <span data-ttu-id="9e8ee-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="9e8ee-629">0x0118</span></span>                                   |
| <span data-ttu-id="9e8ee-630">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-630">Type</span></span>  | <span data-ttu-id="9e8ee-631">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-632">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-632">Count</span></span> | <span data-ttu-id="9e8ee-633">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="9e8ee-634">PropertyTagMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="9e8ee-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="9e8ee-635">Para cada componente de cor, o valor máximo atribuído a esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="9e8ee-636">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-637">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-637">Property info</span></span> | <span data-ttu-id="9e8ee-638">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-639">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-639">Tag</span></span>   | <span data-ttu-id="9e8ee-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="9e8ee-640">0x0119</span></span>                                   |
| <span data-ttu-id="9e8ee-641">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-641">Type</span></span>  | <span data-ttu-id="9e8ee-642">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-643">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-643">Count</span></span> | <span data-ttu-id="9e8ee-644">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="9e8ee-645">PropertyTagXResolution</span><span class="sxs-lookup"><span data-stu-id="9e8ee-645">PropertyTagXResolution</span></span>

<span data-ttu-id="9e8ee-646">Número de pixels por unidade na direção da largura da imagem (x).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="9e8ee-647">A unidade é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-648">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-648">Property info</span></span> | <span data-ttu-id="9e8ee-649">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-650">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-650">Tag</span></span>   | <span data-ttu-id="9e8ee-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-651">0x011A</span></span>                  |
| <span data-ttu-id="9e8ee-652">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-652">Type</span></span>  | <span data-ttu-id="9e8ee-653">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-654">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-654">Count</span></span> | <span data-ttu-id="9e8ee-655">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="9e8ee-656">PropertyTagYResolution</span><span class="sxs-lookup"><span data-stu-id="9e8ee-656">PropertyTagYResolution</span></span>

<span data-ttu-id="9e8ee-657">Número de pixels por unidade na direção da altura da imagem (y).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="9e8ee-658">A unidade é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-659">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-659">Property info</span></span> | <span data-ttu-id="9e8ee-660">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-661">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-661">Tag</span></span>   | <span data-ttu-id="9e8ee-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-662">0x011B</span></span>                  |
| <span data-ttu-id="9e8ee-663">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-663">Type</span></span>  | <span data-ttu-id="9e8ee-664">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-665">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-665">Count</span></span> | <span data-ttu-id="9e8ee-666">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="9e8ee-667">PropertyTagPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="9e8ee-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="9e8ee-668">Se os componentes de pixel são gravados em formato de plana ou de planar.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="9e8ee-669">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-669">Property info</span></span> | <span data-ttu-id="9e8ee-670">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-671">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-671">Tag</span></span>   | <span data-ttu-id="9e8ee-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-672">0x011C</span></span>               |
| <span data-ttu-id="9e8ee-673">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-673">Type</span></span>  | <span data-ttu-id="9e8ee-674">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-675">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-675">Count</span></span> | <span data-ttu-id="9e8ee-676">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="9e8ee-677">PropertyTagPageName</span><span class="sxs-lookup"><span data-stu-id="9e8ee-677">PropertyTagPageName</span></span>

<span data-ttu-id="9e8ee-678">Cadeia de caracteres terminada em nulo que especifica o nome da página da qual a imagem foi verificada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="9e8ee-679">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-679">Property info</span></span> | <span data-ttu-id="9e8ee-680">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-681">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-681">Tag</span></span>   | <span data-ttu-id="9e8ee-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-682">0x011D</span></span>                                             |
| <span data-ttu-id="9e8ee-683">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-683">Type</span></span>  | <span data-ttu-id="9e8ee-684">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-685">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-685">Count</span></span> | <span data-ttu-id="9e8ee-686">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="9e8ee-687">PropertyTagXPosition</span><span class="sxs-lookup"><span data-stu-id="9e8ee-687">PropertyTagXPosition</span></span>

<span data-ttu-id="9e8ee-688">Deslocamento do lado esquerdo da página para o lado esquerdo da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="9e8ee-689">A unidade de medida é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-690">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-690">Property info</span></span> | <span data-ttu-id="9e8ee-691">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-692">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-692">Tag</span></span>   | <span data-ttu-id="9e8ee-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-693">0x011E</span></span>                  |
| <span data-ttu-id="9e8ee-694">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-694">Type</span></span>  | <span data-ttu-id="9e8ee-695">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-696">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-696">Count</span></span> | <span data-ttu-id="9e8ee-697">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="9e8ee-698">PropertyTagYPosition</span><span class="sxs-lookup"><span data-stu-id="9e8ee-698">PropertyTagYPosition</span></span>

<span data-ttu-id="9e8ee-699">Deslocamento da parte superior da página até a parte superior da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="9e8ee-700">A unidade de medida é especificada por [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-701">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-701">Property info</span></span> | <span data-ttu-id="9e8ee-702">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-703">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-703">Tag</span></span>   | <span data-ttu-id="9e8ee-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-704">0x011F</span></span>                  |
| <span data-ttu-id="9e8ee-705">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-705">Type</span></span>  | <span data-ttu-id="9e8ee-706">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-707">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-707">Count</span></span> | <span data-ttu-id="9e8ee-708">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="9e8ee-709">PropertyTagFreeOffset</span><span class="sxs-lookup"><span data-stu-id="9e8ee-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="9e8ee-710">Para cada cadeia de caracteres de bytes não usados contíguos, o deslocamento de byte dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="9e8ee-711">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-711">Property info</span></span> | <span data-ttu-id="9e8ee-712">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="9e8ee-713">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-713">Tag</span></span>  | <span data-ttu-id="9e8ee-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="9e8ee-714">0x0120</span></span>              |
| <span data-ttu-id="9e8ee-715">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-715">Type</span></span> | <span data-ttu-id="9e8ee-716">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="9e8ee-717">PropertyTagFreeByteCounts</span><span class="sxs-lookup"><span data-stu-id="9e8ee-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="9e8ee-718">Para cada cadeia de caracteres de bytes não usados contíguos, o número de bytes nessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="9e8ee-719">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-719">Property info</span></span> | <span data-ttu-id="9e8ee-720">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="9e8ee-721">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-721">Tag</span></span>   | <span data-ttu-id="9e8ee-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="9e8ee-722">0x0121</span></span>                                        |
| <span data-ttu-id="9e8ee-723">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-723">Type</span></span>  | <span data-ttu-id="9e8ee-724">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="9e8ee-725">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-725">Count</span></span> | <span data-ttu-id="9e8ee-726">Número de cadeias de caracteres de bytes não utilizados contíguos.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="9e8ee-727">PropertyTagGrayResponseUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="9e8ee-728">Precisão do número especificado por PropertyTagGrayResponseCurve.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="9e8ee-729">1 especifica décimos, 2 especifica centésimos, 3 especifica milésimos de milhares e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="9e8ee-730">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-730">Property info</span></span> | <span data-ttu-id="9e8ee-731">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-732">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-732">Tag</span></span>   | <span data-ttu-id="9e8ee-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="9e8ee-733">0x0122</span></span>               |
| <span data-ttu-id="9e8ee-734">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-734">Type</span></span>  | <span data-ttu-id="9e8ee-735">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-736">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-736">Count</span></span> | <span data-ttu-id="9e8ee-737">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="9e8ee-738">PropertyTagGrayResponseCurve</span><span class="sxs-lookup"><span data-stu-id="9e8ee-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="9e8ee-739">Para cada valor de pixel possível em uma imagem em tons de cinza, a densidade óptica desse valor de pixel.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="9e8ee-740">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-740">Property info</span></span> | <span data-ttu-id="9e8ee-741">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="9e8ee-742">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-742">Tag</span></span>   | <span data-ttu-id="9e8ee-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="9e8ee-743">0x0123</span></span>                          |
| <span data-ttu-id="9e8ee-744">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-744">Type</span></span>  | <span data-ttu-id="9e8ee-745">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="9e8ee-746">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-746">Count</span></span> | <span data-ttu-id="9e8ee-747">Número de valores de pixel possíveis</span><span class="sxs-lookup"><span data-stu-id="9e8ee-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="9e8ee-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="9e8ee-748">PropertyTagT4Option</span></span>

<span data-ttu-id="9e8ee-749">Conjunto de sinalizadores relacionados à codificação T4.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="9e8ee-750">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-750">Property info</span></span> | <span data-ttu-id="9e8ee-751">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-752">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-752">Tag</span></span>   | <span data-ttu-id="9e8ee-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="9e8ee-753">0x0124</span></span>              |
| <span data-ttu-id="9e8ee-754">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-754">Type</span></span>  | <span data-ttu-id="9e8ee-755">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-756">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-756">Count</span></span> | <span data-ttu-id="9e8ee-757">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="9e8ee-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="9e8ee-758">PropertyTagT6Option</span></span>

<span data-ttu-id="9e8ee-759">Conjunto de sinalizadores relacionados à codificação T6.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="9e8ee-760">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-760">Property info</span></span> | <span data-ttu-id="9e8ee-761">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-762">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-762">Tag</span></span>   | <span data-ttu-id="9e8ee-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="9e8ee-763">0x0125</span></span>              |
| <span data-ttu-id="9e8ee-764">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-764">Type</span></span>  | <span data-ttu-id="9e8ee-765">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-766">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-766">Count</span></span> | <span data-ttu-id="9e8ee-767">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="9e8ee-768">PropertyTagResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="9e8ee-769">Unidade de medida para a resolução horizontal e a resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="9e8ee-770">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-770">Tag</span></span>

<span data-ttu-id="9e8ee-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="9e8ee-771">0x0128</span></span>

<span data-ttu-id="9e8ee-772">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-772">Type</span></span>

<span data-ttu-id="9e8ee-773">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-774">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-774">Count</span></span>

<span data-ttu-id="9e8ee-775">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-775">1</span></span>

<span data-ttu-id="9e8ee-776">2 polegadas e 3 centímetros</span><span class="sxs-lookup"><span data-stu-id="9e8ee-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="9e8ee-777">PropertyTagPageNumber</span><span class="sxs-lookup"><span data-stu-id="9e8ee-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="9e8ee-778">Número de página da página da qual a imagem foi verificada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="9e8ee-779">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-779">Property info</span></span> | <span data-ttu-id="9e8ee-780">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-781">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-781">Tag</span></span>   | <span data-ttu-id="9e8ee-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="9e8ee-782">0x0129</span></span>               |
| <span data-ttu-id="9e8ee-783">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-783">Type</span></span>  | <span data-ttu-id="9e8ee-784">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-785">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-785">Count</span></span> | <span data-ttu-id="9e8ee-786">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="9e8ee-787">PropertyTagTransferFunction</span><span class="sxs-lookup"><span data-stu-id="9e8ee-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="9e8ee-788">Tabelas que especificam funções de transferência para a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="9e8ee-789">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-789">Property info</span></span> | <span data-ttu-id="9e8ee-790">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="9e8ee-791">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-791">Tag</span></span>   | <span data-ttu-id="9e8ee-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-792">0x012D</span></span>                                               |
| <span data-ttu-id="9e8ee-793">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-793">Type</span></span>  | <span data-ttu-id="9e8ee-794">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="9e8ee-795">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-795">Count</span></span> | <span data-ttu-id="9e8ee-796">Número total de palavras de 16 bits necessárias para as tabelas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="9e8ee-797">PropertyTagSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="9e8ee-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="9e8ee-798">Cadeia de caracteres terminada em nulo que especifica o nome e a versão do software ou firmware do dispositivo usado para gerar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="9e8ee-799">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-799">Property info</span></span> | <span data-ttu-id="9e8ee-800">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-801">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-801">Tag</span></span>   | <span data-ttu-id="9e8ee-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="9e8ee-802">0x0131</span></span>                                             |
| <span data-ttu-id="9e8ee-803">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-803">Type</span></span>  | <span data-ttu-id="9e8ee-804">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-805">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-805">Count</span></span> | <span data-ttu-id="9e8ee-806">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="9e8ee-807">PropertyTagDateTime</span><span class="sxs-lookup"><span data-stu-id="9e8ee-807">PropertyTagDateTime</span></span>

<span data-ttu-id="9e8ee-808">Data e hora em que a imagem foi criada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-808">Date and time the image was created.</span></span>



| <span data-ttu-id="9e8ee-809">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-809">Property info</span></span> | <span data-ttu-id="9e8ee-810">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-811">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-811">Tag</span></span>   | <span data-ttu-id="9e8ee-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="9e8ee-812">0x0132</span></span>               |
| <span data-ttu-id="9e8ee-813">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-813">Type</span></span>  | <span data-ttu-id="9e8ee-814">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-815">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-815">Count</span></span> | <span data-ttu-id="9e8ee-816">20</span><span class="sxs-lookup"><span data-stu-id="9e8ee-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="9e8ee-817">PropertyTagArtist</span><span class="sxs-lookup"><span data-stu-id="9e8ee-817">PropertyTagArtist</span></span>

<span data-ttu-id="9e8ee-818">Cadeia de caracteres terminada em nulo que especifica o nome da pessoa que criou a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="9e8ee-819">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-819">Property info</span></span> | <span data-ttu-id="9e8ee-820">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-821">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-821">Tag</span></span>   | <span data-ttu-id="9e8ee-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-822">0x013B</span></span>                                             |
| <span data-ttu-id="9e8ee-823">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-823">Type</span></span>  | <span data-ttu-id="9e8ee-824">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-825">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-825">Count</span></span> | <span data-ttu-id="9e8ee-826">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="9e8ee-827">PropertyTagHostComputer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="9e8ee-828">Cadeia de caracteres terminada em nulo que especifica o computador e/ou sistema operacional usado para criar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="9e8ee-829">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-829">Property info</span></span> | <span data-ttu-id="9e8ee-830">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-831">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-831">Tag</span></span>   | <span data-ttu-id="9e8ee-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-832">0x013C</span></span>                                             |
| <span data-ttu-id="9e8ee-833">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-833">Type</span></span>  | <span data-ttu-id="9e8ee-834">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-835">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-835">Count</span></span> | <span data-ttu-id="9e8ee-836">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="9e8ee-837">PropertyTagPredictor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-837">PropertyTagPredictor</span></span>

<span data-ttu-id="9e8ee-838">Tipo de esquema de previsão que foi aplicado aos dados da imagem antes da aplicação do esquema de codificação.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="9e8ee-839">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-839">Property info</span></span> | <span data-ttu-id="9e8ee-840">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-841">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-841">Tag</span></span>   | <span data-ttu-id="9e8ee-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-842">0x013D</span></span>               |
| <span data-ttu-id="9e8ee-843">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-843">Type</span></span>  | <span data-ttu-id="9e8ee-844">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-845">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-845">Count</span></span> | <span data-ttu-id="9e8ee-846">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="9e8ee-847">PropertyTagWhitePoint</span><span class="sxs-lookup"><span data-stu-id="9e8ee-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="9e8ee-848">A desvio do ponto branco da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="9e8ee-849">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-849">Property info</span></span> | <span data-ttu-id="9e8ee-850">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-851">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-851">Tag</span></span>   | <span data-ttu-id="9e8ee-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-852">0x013E</span></span>                  |
| <span data-ttu-id="9e8ee-853">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-853">Type</span></span>  | <span data-ttu-id="9e8ee-854">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-855">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-855">Count</span></span> | <span data-ttu-id="9e8ee-856">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="9e8ee-857">PropertyTagPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="9e8ee-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="9e8ee-858">Para cada uma das três cores primárias na imagem, a desvio dessa cor.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="9e8ee-859">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-859">Property info</span></span> | <span data-ttu-id="9e8ee-860">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-861">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-861">Tag</span></span>   | <span data-ttu-id="9e8ee-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-862">0x013F</span></span>                  |
| <span data-ttu-id="9e8ee-863">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-863">Type</span></span>  | <span data-ttu-id="9e8ee-864">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-865">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-865">Count</span></span> | <span data-ttu-id="9e8ee-866">6</span><span class="sxs-lookup"><span data-stu-id="9e8ee-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="9e8ee-867">PropertyTagColorMap</span><span class="sxs-lookup"><span data-stu-id="9e8ee-867">PropertyTagColorMap</span></span>

<span data-ttu-id="9e8ee-868">Paleta de cores (tabela de pesquisa) para uma imagem indexada por paleta.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="9e8ee-869">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-869">Property info</span></span> | <span data-ttu-id="9e8ee-870">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="9e8ee-871">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-871">Tag</span></span>   | <span data-ttu-id="9e8ee-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="9e8ee-872">0x0140</span></span>                                          |
| <span data-ttu-id="9e8ee-873">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-873">Type</span></span>  | <span data-ttu-id="9e8ee-874">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="9e8ee-875">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-875">Count</span></span> | <span data-ttu-id="9e8ee-876">Número de palavras de 16 bits necessárias para a paleta</span><span class="sxs-lookup"><span data-stu-id="9e8ee-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="9e8ee-877">PropertyTagHalftoneHints</span><span class="sxs-lookup"><span data-stu-id="9e8ee-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="9e8ee-878">Informações usadas pela função de meio-tom</span><span class="sxs-lookup"><span data-stu-id="9e8ee-878">Information used by the halftone function</span></span>



| <span data-ttu-id="9e8ee-879">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-879">Property info</span></span> | <span data-ttu-id="9e8ee-880">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-881">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-881">Tag</span></span>   | <span data-ttu-id="9e8ee-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="9e8ee-882">0x0141</span></span>               |
| <span data-ttu-id="9e8ee-883">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-883">Type</span></span>  | <span data-ttu-id="9e8ee-884">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-885">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-885">Count</span></span> | <span data-ttu-id="9e8ee-886">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="9e8ee-887">PropertyTagTileWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="9e8ee-888">Número de colunas de pixel em cada bloco.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="9e8ee-889">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-889">Property info</span></span> | <span data-ttu-id="9e8ee-890">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-891">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-891">Tag</span></span>   | <span data-ttu-id="9e8ee-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="9e8ee-892">0x0142</span></span>                                      |
| <span data-ttu-id="9e8ee-893">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-893">Type</span></span>  | <span data-ttu-id="9e8ee-894">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-895">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-895">Count</span></span> | <span data-ttu-id="9e8ee-896">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="9e8ee-897">PropertyTagTileLength</span><span class="sxs-lookup"><span data-stu-id="9e8ee-897">PropertyTagTileLength</span></span>

<span data-ttu-id="9e8ee-898">Número de linhas de pixel em cada bloco.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="9e8ee-899">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-899">Property info</span></span> | <span data-ttu-id="9e8ee-900">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-901">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-901">Tag</span></span>   | <span data-ttu-id="9e8ee-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="9e8ee-902">0x0143</span></span>                                      |
| <span data-ttu-id="9e8ee-903">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-903">Type</span></span>  | <span data-ttu-id="9e8ee-904">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-905">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-905">Count</span></span> | <span data-ttu-id="9e8ee-906">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="9e8ee-907">PropertyTagTileOffset</span><span class="sxs-lookup"><span data-stu-id="9e8ee-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="9e8ee-908">Para cada bloco, o deslocamento de byte desse bloco.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="9e8ee-909">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-909">Property info</span></span> | <span data-ttu-id="9e8ee-910">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-911">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-911">Tag</span></span>   | <span data-ttu-id="9e8ee-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="9e8ee-912">0x0144</span></span>              |
| <span data-ttu-id="9e8ee-913">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-913">Type</span></span>  | <span data-ttu-id="9e8ee-914">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-915">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-915">Count</span></span> | <span data-ttu-id="9e8ee-916">Número de blocos</span><span class="sxs-lookup"><span data-stu-id="9e8ee-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="9e8ee-917">PropertyTagTileByteCounts</span><span class="sxs-lookup"><span data-stu-id="9e8ee-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="9e8ee-918">Para cada bloco, o número de bytes nesse bloco.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="9e8ee-919">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-919">Property info</span></span> | <span data-ttu-id="9e8ee-920">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-921">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-921">Tag</span></span>   | <span data-ttu-id="9e8ee-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="9e8ee-922">0x0145</span></span>                                      |
| <span data-ttu-id="9e8ee-923">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-923">Type</span></span>  | <span data-ttu-id="9e8ee-924">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-925">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-925">Count</span></span> | <span data-ttu-id="9e8ee-926">Número de blocos</span><span class="sxs-lookup"><span data-stu-id="9e8ee-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="9e8ee-927">PropertyTagInkSet</span><span class="sxs-lookup"><span data-stu-id="9e8ee-927">PropertyTagInkSet</span></span>

<span data-ttu-id="9e8ee-928">Conjunto de tintas usadas em uma imagem separada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="9e8ee-929">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-929">Property info</span></span> | <span data-ttu-id="9e8ee-930">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-931">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-931">Tag</span></span>   | <span data-ttu-id="9e8ee-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-932">0x014C</span></span>               |
| <span data-ttu-id="9e8ee-933">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-933">Type</span></span>  | <span data-ttu-id="9e8ee-934">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-935">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-935">Count</span></span> | <span data-ttu-id="9e8ee-936">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="9e8ee-937">PropertyTagInkNames</span><span class="sxs-lookup"><span data-stu-id="9e8ee-937">PropertyTagInkNames</span></span>

<span data-ttu-id="9e8ee-938">Sequência de cadeias de caracteres concatenadas, terminadas em nulo, que especificam os nomes das tintas usadas em uma imagem separada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="9e8ee-939">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-939">Property info</span></span> | <span data-ttu-id="9e8ee-940">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="9e8ee-941">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-941">Tag</span></span>   | <span data-ttu-id="9e8ee-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="9e8ee-943">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-943">Type</span></span>  | <span data-ttu-id="9e8ee-944">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="9e8ee-945">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-945">Count</span></span> | <span data-ttu-id="9e8ee-946">Comprimento total da sequência de cadeias de caracteres, incluindo os terminadores nulos</span><span class="sxs-lookup"><span data-stu-id="9e8ee-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="9e8ee-947">PropertyTagNumberOfInks</span><span class="sxs-lookup"><span data-stu-id="9e8ee-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="9e8ee-948">Número de tintas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-948">Number of inks.</span></span>



| <span data-ttu-id="9e8ee-949">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-949">Property info</span></span> | <span data-ttu-id="9e8ee-950">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-951">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-951">Tag</span></span>   | <span data-ttu-id="9e8ee-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-952">0x014E</span></span>               |
| <span data-ttu-id="9e8ee-953">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-953">Type</span></span>  | <span data-ttu-id="9e8ee-954">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-955">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-955">Count</span></span> | <span data-ttu-id="9e8ee-956">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="9e8ee-957">PropertyTagDotRange</span><span class="sxs-lookup"><span data-stu-id="9e8ee-957">PropertyTagDotRange</span></span>

<span data-ttu-id="9e8ee-958">Valores de componente de cor que correspondem a um ponto de 0% e um ponto de 100 por cento.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="9e8ee-959">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-959">Property info</span></span> | <span data-ttu-id="9e8ee-960">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-961">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-961">Tag</span></span>   | <span data-ttu-id="9e8ee-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="9e8ee-962">0x0150</span></span>                                      |
| <span data-ttu-id="9e8ee-963">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-963">Type</span></span>  | <span data-ttu-id="9e8ee-964">PropertyTagTypeByte ou PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-965">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-965">Count</span></span> | <span data-ttu-id="9e8ee-966">2 ou 2 × PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="9e8ee-967">PropertyTagTargetPrinter</span><span class="sxs-lookup"><span data-stu-id="9e8ee-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="9e8ee-968">Cadeia de caracteres terminada em nulo que descreve o ambiente de impressão pretendido.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="9e8ee-969">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-969">Property info</span></span> | <span data-ttu-id="9e8ee-970">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-971">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-971">Tag</span></span>   | <span data-ttu-id="9e8ee-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="9e8ee-972">0x0151</span></span>                                             |
| <span data-ttu-id="9e8ee-973">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-973">Type</span></span>  | <span data-ttu-id="9e8ee-974">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-975">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-975">Count</span></span> | <span data-ttu-id="9e8ee-976">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="9e8ee-977">PropertyTagExtraSamples</span><span class="sxs-lookup"><span data-stu-id="9e8ee-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="9e8ee-978">Número de componentes de cores extras.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-978">Number of extra color components.</span></span> <span data-ttu-id="9e8ee-979">Por exemplo, um componente extra pode conter um valor alfa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="9e8ee-980">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-980">Property info</span></span> | <span data-ttu-id="9e8ee-981">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-982">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-982">Tag</span></span>   | <span data-ttu-id="9e8ee-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="9e8ee-983">0x0152</span></span>               |
| <span data-ttu-id="9e8ee-984">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-984">Type</span></span>  | <span data-ttu-id="9e8ee-985">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-986">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-986">Count</span></span> | <span data-ttu-id="9e8ee-987">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="9e8ee-988">PropertyTagSampleFormat</span><span class="sxs-lookup"><span data-stu-id="9e8ee-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="9e8ee-989">Para cada componente de cor, o formato numérico (sem sinal, assinado, ponto flutuante) desse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="9e8ee-990">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-991">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-991">Property info</span></span> | <span data-ttu-id="9e8ee-992">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-993">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-993">Tag</span></span>   | <span data-ttu-id="9e8ee-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="9e8ee-994">0x0153</span></span>                                   |
| <span data-ttu-id="9e8ee-995">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-995">Type</span></span>  | <span data-ttu-id="9e8ee-996">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-997">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-997">Count</span></span> | <span data-ttu-id="9e8ee-998">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="9e8ee-999">PropertyTagSMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="9e8ee-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="9e8ee-1000">Para cada componente de cor, o valor mínimo desse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="9e8ee-1001">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1002">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1002">Property info</span></span> | <span data-ttu-id="9e8ee-1003">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="9e8ee-1004">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1004">Tag</span></span>   | <span data-ttu-id="9e8ee-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1005">0x0154</span></span>                                              |
| <span data-ttu-id="9e8ee-1006">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1006">Type</span></span>  | <span data-ttu-id="9e8ee-1007">O tipo que melhor corresponde aos dados do componente de pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="9e8ee-1008">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1008">Count</span></span> | <span data-ttu-id="9e8ee-1009">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="9e8ee-1010">PropertyTagSMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="9e8ee-1011">Para cada componente de cor, o valor máximo desse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="9e8ee-1012">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1013">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1013">Property info</span></span> | <span data-ttu-id="9e8ee-1014">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="9e8ee-1015">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1015">Tag</span></span>   | <span data-ttu-id="9e8ee-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1016">0x0155</span></span>                                              |
| <span data-ttu-id="9e8ee-1017">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1017">Type</span></span>  | <span data-ttu-id="9e8ee-1018">O tipo que melhor corresponde aos dados do componente de pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="9e8ee-1019">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1019">Count</span></span> | <span data-ttu-id="9e8ee-1020">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="9e8ee-1021">PropertyTagTransferRange</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="9e8ee-1022">Tabela de valores que estende o intervalo da função de transferência.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="9e8ee-1023">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1023">Property info</span></span> | <span data-ttu-id="9e8ee-1024">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1025">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1025">Tag</span></span>   | <span data-ttu-id="9e8ee-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1026">0x0156</span></span>               |
| <span data-ttu-id="9e8ee-1027">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1027">Type</span></span>  | <span data-ttu-id="9e8ee-1028">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1029">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1029">Count</span></span> | <span data-ttu-id="9e8ee-1030">6</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="9e8ee-1031">PropertyTagJPEGProc</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="9e8ee-1032">Processo de compactação JPEG.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1032">JPEG compression process.</span></span>



| <span data-ttu-id="9e8ee-1033">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1033">Property info</span></span> | <span data-ttu-id="9e8ee-1034">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1035">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1035">Tag</span></span>   | <span data-ttu-id="9e8ee-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1036">0x0200</span></span>               |
| <span data-ttu-id="9e8ee-1037">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1037">Type</span></span>  | <span data-ttu-id="9e8ee-1038">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1039">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1039">Count</span></span> | <span data-ttu-id="9e8ee-1040">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="9e8ee-1041">PropertyTagJPEGInterFormat</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="9e8ee-1042">Offset para o início de um fragmentado de JPEG.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="9e8ee-1043">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1043">Property info</span></span> | <span data-ttu-id="9e8ee-1044">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1045">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1045">Tag</span></span>   | <span data-ttu-id="9e8ee-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1046">0x0201</span></span>              |
| <span data-ttu-id="9e8ee-1047">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1047">Type</span></span>  | <span data-ttu-id="9e8ee-1048">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1049">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1049">Count</span></span> | <span data-ttu-id="9e8ee-1050">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="9e8ee-1051">PropertyTagJPEGInterLength</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="9e8ee-1052">Comprimento, em bytes, do JPEG fragmentado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="9e8ee-1053">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1053">Property info</span></span> | <span data-ttu-id="9e8ee-1054">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1055">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1055">Tag</span></span>   | <span data-ttu-id="9e8ee-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1056">0x0202</span></span>              |
| <span data-ttu-id="9e8ee-1057">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1057">Type</span></span>  | <span data-ttu-id="9e8ee-1058">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1059">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1059">Count</span></span> | <span data-ttu-id="9e8ee-1060">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="9e8ee-1061">PropertyTagJPEGRestartInterval</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="9e8ee-1062">Comprimento do intervalo de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="9e8ee-1063">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1063">Property info</span></span> | <span data-ttu-id="9e8ee-1064">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1065">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1065">Tag</span></span>   | <span data-ttu-id="9e8ee-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1066">0x0203</span></span>               |
| <span data-ttu-id="9e8ee-1067">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1067">Type</span></span>  | <span data-ttu-id="9e8ee-1068">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1069">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1069">Count</span></span> | <span data-ttu-id="9e8ee-1070">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="9e8ee-1071">PropertyTagJPEGLosslessPredictors</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="9e8ee-1072">Para cada componente de cor, um valor de seleção de pregnóstico sem perdas para esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="9e8ee-1073">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1074">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1074">Property info</span></span> | <span data-ttu-id="9e8ee-1075">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-1076">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1076">Tag</span></span>   | <span data-ttu-id="9e8ee-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1077">0x0205</span></span>                                   |
| <span data-ttu-id="9e8ee-1078">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1078">Type</span></span>  | <span data-ttu-id="9e8ee-1079">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-1080">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1080">Count</span></span> | <span data-ttu-id="9e8ee-1081">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="9e8ee-1082">PropertyTagJPEGPointTransforms</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="9e8ee-1083">Para cada componente de cor, um valor de transformação de ponto para esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="9e8ee-1084">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1085">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1085">Property info</span></span> | <span data-ttu-id="9e8ee-1086">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-1087">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1087">Tag</span></span>   | <span data-ttu-id="9e8ee-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1088">0x0206</span></span>                                   |
| <span data-ttu-id="9e8ee-1089">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1089">Type</span></span>  | <span data-ttu-id="9e8ee-1090">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="9e8ee-1091">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1091">Count</span></span> | <span data-ttu-id="9e8ee-1092">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="9e8ee-1093">PropertyTagJPEGQTables</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="9e8ee-1094">Para cada componente de cor, o deslocamento para a tabela de quantificação para esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="9e8ee-1095">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1096">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1096">Property info</span></span> | <span data-ttu-id="9e8ee-1097">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-1098">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1098">Tag</span></span>   | <span data-ttu-id="9e8ee-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1099">0x0207</span></span>                                   |
| <span data-ttu-id="9e8ee-1100">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1100">Type</span></span>  | <span data-ttu-id="9e8ee-1101">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="9e8ee-1102">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1102">Count</span></span> | <span data-ttu-id="9e8ee-1103">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="9e8ee-1104">PropertyTagJPEGDCTables</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="9e8ee-1105">Para cada componente de cor, o deslocamento para a tabela de Huffman de DC (ou tabela de Huffman sem perdas) para esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="9e8ee-1106">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1107">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1107">Property info</span></span> | <span data-ttu-id="9e8ee-1108">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-1109">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1109">Tag</span></span>   | <span data-ttu-id="9e8ee-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1110">0x0208</span></span>                                   |
| <span data-ttu-id="9e8ee-1111">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1111">Type</span></span>  | <span data-ttu-id="9e8ee-1112">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="9e8ee-1113">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1113">Count</span></span> | <span data-ttu-id="9e8ee-1114">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="9e8ee-1115">PropertyTagJPEGACTables</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="9e8ee-1116">Para cada componente de cor, o deslocamento para a tabela de Huffman de AC para esse componente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="9e8ee-1117">Consulte também [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1118">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1118">Property info</span></span> | <span data-ttu-id="9e8ee-1119">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="9e8ee-1120">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1120">Tag</span></span>   | <span data-ttu-id="9e8ee-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1121">0x0209</span></span>                                   |
| <span data-ttu-id="9e8ee-1122">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1122">Type</span></span>  | <span data-ttu-id="9e8ee-1123">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="9e8ee-1124">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1124">Count</span></span> | <span data-ttu-id="9e8ee-1125">Número de amostras (componentes) por pixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="9e8ee-1126">PropertyTagYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="9e8ee-1127">Coeficientes para transformação de RGB para dados de imagem YCbCr.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="9e8ee-1128">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1128">Property info</span></span> | <span data-ttu-id="9e8ee-1129">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1130">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1130">Tag</span></span>   | <span data-ttu-id="9e8ee-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1131">0x0211</span></span>                  |
| <span data-ttu-id="9e8ee-1132">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1132">Type</span></span>  | <span data-ttu-id="9e8ee-1133">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1134">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1134">Count</span></span> | <span data-ttu-id="9e8ee-1135">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="9e8ee-1136">PropertyTagYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="9e8ee-1137">Taxa de amostragem de componentes crominância em relação ao componente de luminância.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="9e8ee-1138">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1138">Property info</span></span> | <span data-ttu-id="9e8ee-1139">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1140">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1140">Tag</span></span>   | <span data-ttu-id="9e8ee-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1141">0x0212</span></span>               |
| <span data-ttu-id="9e8ee-1142">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1142">Type</span></span>  | <span data-ttu-id="9e8ee-1143">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1144">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1144">Count</span></span> | <span data-ttu-id="9e8ee-1145">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="9e8ee-1146">PropertyTagYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="9e8ee-1147">Posição dos componentes do crominância em relação ao componente de luminância.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="9e8ee-1148">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1148">Property info</span></span> | <span data-ttu-id="9e8ee-1149">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1150">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1150">Tag</span></span>   | <span data-ttu-id="9e8ee-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1151">0x0213</span></span>               |
| <span data-ttu-id="9e8ee-1152">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1152">Type</span></span>  | <span data-ttu-id="9e8ee-1153">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1154">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1154">Count</span></span> | <span data-ttu-id="9e8ee-1155">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="9e8ee-1156">PropertyTagREFBlackWhite</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="9e8ee-1157">Valor de ponto preto de referência e valor de ponto branco de referência.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="9e8ee-1158">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1158">Property info</span></span> | <span data-ttu-id="9e8ee-1159">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1160">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1160">Tag</span></span>   | <span data-ttu-id="9e8ee-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1161">0x0214</span></span>                  |
| <span data-ttu-id="9e8ee-1162">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1162">Type</span></span>  | <span data-ttu-id="9e8ee-1163">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1164">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1164">Count</span></span> | <span data-ttu-id="9e8ee-1165">6</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="9e8ee-1166">PropertyTagGamma</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1166">PropertyTagGamma</span></span>

<span data-ttu-id="9e8ee-1167">Valor de gama anexado à imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="9e8ee-1168">O valor de gama é armazenado como um número racional (par de **longo**) com um numerador de 100000.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="9e8ee-1169">Por exemplo, um valor de gama de 2,2 é armazenado como o par (100000, 45455).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="9e8ee-1170">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1170">Property info</span></span> | <span data-ttu-id="9e8ee-1171">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1172">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1172">Tag</span></span>   | <span data-ttu-id="9e8ee-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1173">0x0301</span></span>                  |
| <span data-ttu-id="9e8ee-1174">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1174">Type</span></span>  | <span data-ttu-id="9e8ee-1175">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1176">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1176">Count</span></span> | <span data-ttu-id="9e8ee-1177">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="9e8ee-1178">PropertyTagICCProfileDescriptor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="9e8ee-1179">Cadeia de caracteres terminada em nulo que identifica um perfil ICC.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="9e8ee-1180">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1180">Property info</span></span> | <span data-ttu-id="9e8ee-1181">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1182">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1182">Tag</span></span>   | <span data-ttu-id="9e8ee-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1183">0x0302</span></span>                                             |
| <span data-ttu-id="9e8ee-1184">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1184">Type</span></span>  | <span data-ttu-id="9e8ee-1185">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1186">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1186">Count</span></span> | <span data-ttu-id="9e8ee-1187">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="9e8ee-1188">PropertyTagSRGBRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="9e8ee-1189">Como a imagem deve ser exibida conforme definido pelo consórcio de cor internacional (ICC).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="9e8ee-1190">Se um objeto de  [**imagem**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ for construído com o parâmetro *UseEmbeddedColorManagement* definido como **true**, o GDI+ renderizará a imagem de acordo com a tentativa de renderização especificada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="9e8ee-1191">A intenção pode ser definida como perceptiva, colorimétrico relativo, saturação ou colorimétrico absoluto.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="9e8ee-1192">A intenção perceptiva, que é adequada para fotografias, oferece boa adaptação à gama do dispositivo de vídeo às custas da precisão colorimétrico.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="9e8ee-1193">A intenção colorimétrico relativa é adequada para imagens (por exemplo, logotipos) que exigem correspondência de aparência de cor em relação ao ponto branco do dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="9e8ee-1194">A intenção de saturação, que é adequada para gráficos e grafos, preserva a saturação às custas de matiz e claridade.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="9e8ee-1195">A intenção colorimétrico absoluta é adequada para provas (visualizações de imagens destinadas a um dispositivo de vídeo diferente) que exigem a preservação do colorimetry absoluto.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="9e8ee-1196">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1196">Tag</span></span>

<span data-ttu-id="9e8ee-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1197">0x0303</span></span>

<span data-ttu-id="9e8ee-1198">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1198">Type</span></span>

<span data-ttu-id="9e8ee-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1199">BYTE</span></span>

<span data-ttu-id="9e8ee-1200">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1200">Count</span></span>

<span data-ttu-id="9e8ee-1201">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1201">1</span></span>

<span data-ttu-id="9e8ee-1202">0-perceptiva 1-colorimétrico relativo 2-saturação 3-colorimétrico absoluto</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="9e8ee-1203">PropertyTagImageTitle</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="9e8ee-1204">Cadeia de caracteres terminada em nulo que especifica o título da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="9e8ee-1205">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1205">Property info</span></span> | <span data-ttu-id="9e8ee-1206">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1207">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1207">Tag</span></span>   | <span data-ttu-id="9e8ee-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1208">0x0320</span></span>                                             |
| <span data-ttu-id="9e8ee-1209">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1209">Type</span></span>  | <span data-ttu-id="9e8ee-1210">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1211">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1211">Count</span></span> | <span data-ttu-id="9e8ee-1212">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="9e8ee-1213">PropertyTagResolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="9e8ee-1214">Unidades nas quais exibir a resolução horizontal.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="9e8ee-1215">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1215">Tag</span></span>

<span data-ttu-id="9e8ee-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1216">0x5001</span></span>

<span data-ttu-id="9e8ee-1217">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1217">Type</span></span>

<span data-ttu-id="9e8ee-1218">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1219">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1219">Count</span></span>

<span data-ttu-id="9e8ee-1220">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1220">1</span></span>

<span data-ttu-id="9e8ee-1221">1-pixels por polegada 2-pixels por centímetro</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="9e8ee-1222">PropertyTagResolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="9e8ee-1223">Unidades nas quais exibir a resolução vertical.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="9e8ee-1224">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1224">Tag</span></span>

<span data-ttu-id="9e8ee-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1225">0x5002</span></span>

<span data-ttu-id="9e8ee-1226">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1226">Type</span></span>

<span data-ttu-id="9e8ee-1227">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1228">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1228">Count</span></span>

<span data-ttu-id="9e8ee-1229">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1229">1</span></span>

<span data-ttu-id="9e8ee-1230">1-pixels por polegada 2-pixels por centímetro</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="9e8ee-1231">PropertyTagResolutionXLengthUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="9e8ee-1232">Unidades nas quais exibir a largura da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="9e8ee-1233">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1233">Tag</span></span>

<span data-ttu-id="9e8ee-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1234">0x5003</span></span>

<span data-ttu-id="9e8ee-1235">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1235">Type</span></span>

<span data-ttu-id="9e8ee-1236">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1237">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1237">Count</span></span>

<span data-ttu-id="9e8ee-1238">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1238">1</span></span>

<span data-ttu-id="9e8ee-1239">1-polegadas 2-centímetros 3-pontos 4-paicas 5-colunas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="9e8ee-1240">PropertyTagResolutionYLengthUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="9e8ee-1241">Unidades nas quais exibir a altura da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="9e8ee-1242">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1242">Tag</span></span>

<span data-ttu-id="9e8ee-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1243">0x5004</span></span>

<span data-ttu-id="9e8ee-1244">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1244">Type</span></span>

<span data-ttu-id="9e8ee-1245">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1246">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1246">Count</span></span>

<span data-ttu-id="9e8ee-1247">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1247">1</span></span>

<span data-ttu-id="9e8ee-1248">1-polegadas 2-centímetros 3-pontos 4-paicas 5-colunas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="9e8ee-1249">PropertyTagPrintFlags</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="9e8ee-1250">Sequência de valores Boolianos de um byte que especificam opções de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="9e8ee-1251">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1251">Property info</span></span> | <span data-ttu-id="9e8ee-1252">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1253">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1253">Tag</span></span>   | <span data-ttu-id="9e8ee-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1254">0x5005</span></span>               |
| <span data-ttu-id="9e8ee-1255">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1255">Type</span></span>  | <span data-ttu-id="9e8ee-1256">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-1257">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1257">Count</span></span> | <span data-ttu-id="9e8ee-1258">Número de sinalizadores</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="9e8ee-1259">PropertyTagPrintFlagsVersion</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="9e8ee-1260">Versão de sinalizadores de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1260">Print flags version.</span></span>



| <span data-ttu-id="9e8ee-1261">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1261">Property info</span></span> | <span data-ttu-id="9e8ee-1262">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1263">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1263">Tag</span></span>   | <span data-ttu-id="9e8ee-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1264">0x5006</span></span>               |
| <span data-ttu-id="9e8ee-1265">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1265">Type</span></span>  | <span data-ttu-id="9e8ee-1266">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1267">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1267">Count</span></span> | <span data-ttu-id="9e8ee-1268">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="9e8ee-1269">PropertyTagPrintFlagsCrop</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="9e8ee-1270">Imprimir marcas de corte do centro de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="9e8ee-1271">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1271">Property info</span></span> | <span data-ttu-id="9e8ee-1272">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1273">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1273">Tag</span></span>   | <span data-ttu-id="9e8ee-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1274">0x5007</span></span>              |
| <span data-ttu-id="9e8ee-1275">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1275">Type</span></span>  | <span data-ttu-id="9e8ee-1276">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-1277">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1277">Count</span></span> | <span data-ttu-id="9e8ee-1278">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="9e8ee-1279">PropertyTagPrintFlagsBleedWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="9e8ee-1280">Largura de sangria de sinalizadores de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="9e8ee-1281">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1281">Property info</span></span> | <span data-ttu-id="9e8ee-1282">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1283">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1283">Tag</span></span>   | <span data-ttu-id="9e8ee-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1284">0x5008</span></span>              |
| <span data-ttu-id="9e8ee-1285">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1285">Type</span></span>  | <span data-ttu-id="9e8ee-1286">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1287">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1287">Count</span></span> | <span data-ttu-id="9e8ee-1288">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="9e8ee-1289">PropertyTagPrintFlagsBleedWidthScale</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="9e8ee-1290">Escala da largura de sangria de sinalizadores de impressão.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="9e8ee-1291">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1291">Property info</span></span> | <span data-ttu-id="9e8ee-1292">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1293">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1293">Tag</span></span>   | <span data-ttu-id="9e8ee-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1294">0x5009</span></span>               |
| <span data-ttu-id="9e8ee-1295">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1295">Type</span></span>  | <span data-ttu-id="9e8ee-1296">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1297">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1297">Count</span></span> | <span data-ttu-id="9e8ee-1298">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="9e8ee-1299">PropertyTagHalftoneLPI</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="9e8ee-1300">Frequência de tela da tinta, em linhas por polegada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="9e8ee-1301">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1301">Property info</span></span> | <span data-ttu-id="9e8ee-1302">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1303">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1303">Tag</span></span>   | <span data-ttu-id="9e8ee-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1304">0x500A</span></span>                  |
| <span data-ttu-id="9e8ee-1305">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1305">Type</span></span>  | <span data-ttu-id="9e8ee-1306">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1307">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1307">Count</span></span> | <span data-ttu-id="9e8ee-1308">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="9e8ee-1309">PropertyTagHalftoneLPIUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="9e8ee-1310">Unidades para a frequência da tela.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="9e8ee-1311">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1311">Tag</span></span>

<span data-ttu-id="9e8ee-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1312">0x500B</span></span>

<span data-ttu-id="9e8ee-1313">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1313">Type</span></span>

<span data-ttu-id="9e8ee-1314">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1315">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1315">Count</span></span>

<span data-ttu-id="9e8ee-1316">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1316">1</span></span>

<span data-ttu-id="9e8ee-1317">1-linhas por polegada 2-linhas por centímetro</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="9e8ee-1318">PropertyTagHalftoneDegree</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="9e8ee-1319">Ângulo da tela.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1319">Angle for screen.</span></span>



| <span data-ttu-id="9e8ee-1320">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1320">Property info</span></span> | <span data-ttu-id="9e8ee-1321">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1322">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1322">Tag</span></span>   | <span data-ttu-id="9e8ee-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1323">0x500C</span></span>                  |
| <span data-ttu-id="9e8ee-1324">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1324">Type</span></span>  | <span data-ttu-id="9e8ee-1325">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1326">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1326">Count</span></span> | <span data-ttu-id="9e8ee-1327">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="9e8ee-1328">PropertyTagHalftoneShape</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="9e8ee-1329">Forma dos pontos de retícula.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="9e8ee-1330">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1330">Tag</span></span>

<span data-ttu-id="9e8ee-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1331">0x500D</span></span>

<span data-ttu-id="9e8ee-1332">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1332">Type</span></span>

<span data-ttu-id="9e8ee-1333">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-1334">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1334">Count</span></span>

<span data-ttu-id="9e8ee-1335">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1335">1</span></span>

<span data-ttu-id="9e8ee-1336">0-redondo 1-elipse 2-linha 3-quadrado 4-Cruz 6-losango</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="9e8ee-1337">PropertyTagHalftoneMisc</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="9e8ee-1338">Várias informações de meio-tom.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="9e8ee-1339">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1339">Property info</span></span> | <span data-ttu-id="9e8ee-1340">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1341">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1341">Tag</span></span>   | <span data-ttu-id="9e8ee-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1342">0x500E</span></span>              |
| <span data-ttu-id="9e8ee-1343">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1343">Type</span></span>  | <span data-ttu-id="9e8ee-1344">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1345">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1345">Count</span></span> | <span data-ttu-id="9e8ee-1346">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="9e8ee-1347">PropertyTagHalftoneScreen</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="9e8ee-1348">Valor booliano que especifica se as telas padrão da impressora devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="9e8ee-1349">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1349">Tag</span></span>

<span data-ttu-id="9e8ee-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1350">0x500F</span></span>

<span data-ttu-id="9e8ee-1351">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1351">Type</span></span>

<span data-ttu-id="9e8ee-1352">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="9e8ee-1353">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1353">Count</span></span>

<span data-ttu-id="9e8ee-1354">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1354">1</span></span>

<span data-ttu-id="9e8ee-1355">1-usar as telas padrão 2-outras da impressora</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="9e8ee-1356">PropertyTagJPEGQuality</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="9e8ee-1357">Marca particular usada pelo formato Adobe Photoshop.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="9e8ee-1358">Não destinado ao uso público.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1358">Not for public use.</span></span>



| <span data-ttu-id="9e8ee-1359">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1359">Property info</span></span> | <span data-ttu-id="9e8ee-1360">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1361">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1361">Tag</span></span>   | <span data-ttu-id="9e8ee-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1362">0x5010</span></span>               |
| <span data-ttu-id="9e8ee-1363">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1363">Type</span></span>  | <span data-ttu-id="9e8ee-1364">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1365">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1365">Count</span></span> | <span data-ttu-id="9e8ee-1366">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="9e8ee-1367">PropertyTagGridSize</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="9e8ee-1368">Bloco de informações sobre grades e guias.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="9e8ee-1369">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1369">Property info</span></span> | <span data-ttu-id="9e8ee-1370">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-1371">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1371">Tag</span></span>   | <span data-ttu-id="9e8ee-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1372">0x5011</span></span>                   |
| <span data-ttu-id="9e8ee-1373">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1373">Type</span></span>  | <span data-ttu-id="9e8ee-1374">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-1375">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1375">Count</span></span> | <span data-ttu-id="9e8ee-1376">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="9e8ee-1377">PropertyTagThumbnailFormat</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="9e8ee-1378">Formato da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="9e8ee-1379">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1379">Tag</span></span>

<span data-ttu-id="9e8ee-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1380">0x5012</span></span>

<span data-ttu-id="9e8ee-1381">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1381">Type</span></span>

<span data-ttu-id="9e8ee-1382">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="9e8ee-1383">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1383">Count</span></span>

<span data-ttu-id="9e8ee-1384">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1384">1</span></span>

<span data-ttu-id="9e8ee-1385">0-RGB bruto 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="9e8ee-1386">PropertyTagThumbnailWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="9e8ee-1387">Largura, em pixels, da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1388">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1388">Property info</span></span> | <span data-ttu-id="9e8ee-1389">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1390">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1390">Tag</span></span>   | <span data-ttu-id="9e8ee-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1391">0x5013</span></span>              |
| <span data-ttu-id="9e8ee-1392">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1392">Type</span></span>  | <span data-ttu-id="9e8ee-1393">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1394">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1394">Count</span></span> | <span data-ttu-id="9e8ee-1395">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="9e8ee-1396">PropertyTagThumbnailHeight</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="9e8ee-1397">Altura, em pixels, da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1398">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1398">Property info</span></span> | <span data-ttu-id="9e8ee-1399">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1400">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1400">Tag</span></span>   | <span data-ttu-id="9e8ee-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1401">0x5014</span></span>              |
| <span data-ttu-id="9e8ee-1402">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1402">Type</span></span>  | <span data-ttu-id="9e8ee-1403">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1404">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1404">Count</span></span> | <span data-ttu-id="9e8ee-1405">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="9e8ee-1406">PropertyTagThumbnailColorDepth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="9e8ee-1407">bits por pixel (BPP) para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1408">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1408">Property info</span></span> | <span data-ttu-id="9e8ee-1409">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1410">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1410">Tag</span></span>   | <span data-ttu-id="9e8ee-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1411">0x5015</span></span>               |
| <span data-ttu-id="9e8ee-1412">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1412">Type</span></span>  | <span data-ttu-id="9e8ee-1413">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1414">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1414">Count</span></span> | <span data-ttu-id="9e8ee-1415">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="9e8ee-1416">PropertyTagThumbnailPlanes</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="9e8ee-1417">Número de planos de cores para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1418">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1418">Property info</span></span> | <span data-ttu-id="9e8ee-1419">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1420">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1420">Tag</span></span>   | <span data-ttu-id="9e8ee-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1421">0x5016</span></span>               |
| <span data-ttu-id="9e8ee-1422">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1422">Type</span></span>  | <span data-ttu-id="9e8ee-1423">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1424">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1424">Count</span></span> | <span data-ttu-id="9e8ee-1425">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="9e8ee-1426">PropertyTagThumbnailRawBytes</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="9e8ee-1427">Deslocamento de bytes entre linhas de dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="9e8ee-1428">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1428">Property info</span></span> | <span data-ttu-id="9e8ee-1429">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1430">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1430">Tag</span></span>   | <span data-ttu-id="9e8ee-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1431">0x5017</span></span>              |
| <span data-ttu-id="9e8ee-1432">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1432">Type</span></span>  | <span data-ttu-id="9e8ee-1433">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1434">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1434">Count</span></span> | <span data-ttu-id="9e8ee-1435">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="9e8ee-1436">PropertyTagThumbnailSize</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="9e8ee-1437">Tamanho total, em bytes, da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1438">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1438">Property info</span></span> | <span data-ttu-id="9e8ee-1439">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1440">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1440">Tag</span></span>   | <span data-ttu-id="9e8ee-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1441">0x5018</span></span>              |
| <span data-ttu-id="9e8ee-1442">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1442">Type</span></span>  | <span data-ttu-id="9e8ee-1443">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1444">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1444">Count</span></span> | <span data-ttu-id="9e8ee-1445">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="9e8ee-1446">PropertyTagThumbnailCompressedSize</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="9e8ee-1447">Tamanho compactado, em bytes, da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1448">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1448">Property info</span></span> | <span data-ttu-id="9e8ee-1449">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1450">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1450">Tag</span></span>   | <span data-ttu-id="9e8ee-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1451">0x5019</span></span>              |
| <span data-ttu-id="9e8ee-1452">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1452">Type</span></span>  | <span data-ttu-id="9e8ee-1453">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1454">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1454">Count</span></span> | <span data-ttu-id="9e8ee-1455">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="9e8ee-1456">PropertyTagColorTransferFunction</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="9e8ee-1457">Tabela de valores que especificam funções de transferência de cor.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="9e8ee-1458">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1458">Property info</span></span> | <span data-ttu-id="9e8ee-1459">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-1460">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1460">Tag</span></span>   | <span data-ttu-id="9e8ee-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1461">0x501A</span></span>                   |
| <span data-ttu-id="9e8ee-1462">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1462">Type</span></span>  | <span data-ttu-id="9e8ee-1463">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-1464">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1464">Count</span></span> | <span data-ttu-id="9e8ee-1465">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="9e8ee-1466">PropertyTagThumbnailData</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="9e8ee-1467">Bits de miniatura bruta no formato JPEG ou RGB.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="9e8ee-1468">Depende de PropertyTagThumbnailFormat.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="9e8ee-1469">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1469">Property info</span></span> | <span data-ttu-id="9e8ee-1470">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1471">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1471">Tag</span></span>   | <span data-ttu-id="9e8ee-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1472">0x501B</span></span>              |
| <span data-ttu-id="9e8ee-1473">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1473">Type</span></span>  | <span data-ttu-id="9e8ee-1474">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-1475">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1475">Count</span></span> | <span data-ttu-id="9e8ee-1476">Variável</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="9e8ee-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="9e8ee-1478">Número de pixels por linha na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1479">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1479">Property info</span></span> | <span data-ttu-id="9e8ee-1480">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-1481">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1481">Tag</span></span>   | <span data-ttu-id="9e8ee-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1482">0x5020</span></span>                                      |
| <span data-ttu-id="9e8ee-1483">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1483">Type</span></span>  | <span data-ttu-id="9e8ee-1484">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1485">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1485">Count</span></span> | <span data-ttu-id="9e8ee-1486">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="9e8ee-1487">PropertyTagThumbnailImageHeight</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="9e8ee-1488">Número de linhas de pixel na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1489">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1489">Property info</span></span> | <span data-ttu-id="9e8ee-1490">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-1491">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1491">Tag</span></span>   | <span data-ttu-id="9e8ee-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1492">0x5021</span></span>                                      |
| <span data-ttu-id="9e8ee-1493">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1493">Type</span></span>  | <span data-ttu-id="9e8ee-1494">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1495">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1495">Count</span></span> | <span data-ttu-id="9e8ee-1496">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="9e8ee-1497">PropertyTagThumbnailBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="9e8ee-1498">Número de bits por componente de cor na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1499">Consulte também [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="9e8ee-1500">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1500">Property info</span></span> | <span data-ttu-id="9e8ee-1501">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="9e8ee-1502">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1502">Tag</span></span>   | <span data-ttu-id="9e8ee-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="9e8ee-1504">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1504">Type</span></span>  | <span data-ttu-id="9e8ee-1505">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="9e8ee-1506">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1506">Count</span></span> | <span data-ttu-id="9e8ee-1507">Número de amostras (componentes) por pixel na imagem em miniatura</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="9e8ee-1508">PropertyTagThumbnailCompression</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="9e8ee-1509">Esquema de compactação usado para dados de imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="9e8ee-1510">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1510">Property info</span></span> | <span data-ttu-id="9e8ee-1511">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1512">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1512">Tag</span></span>   | <span data-ttu-id="9e8ee-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1513">0x5023</span></span>               |
| <span data-ttu-id="9e8ee-1514">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1514">Type</span></span>  | <span data-ttu-id="9e8ee-1515">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1516">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1516">Count</span></span> | <span data-ttu-id="9e8ee-1517">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="9e8ee-1518">PropertyTagThumbnailPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="9e8ee-1519">Como os dados de pixel de miniatura serão interpretados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="9e8ee-1520">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1520">Property info</span></span> | <span data-ttu-id="9e8ee-1521">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1522">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1522">Tag</span></span>   | <span data-ttu-id="9e8ee-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1523">0x5024</span></span>               |
| <span data-ttu-id="9e8ee-1524">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1524">Type</span></span>  | <span data-ttu-id="9e8ee-1525">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1526">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1526">Count</span></span> | <span data-ttu-id="9e8ee-1527">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="9e8ee-1528">PropertyTagThumbnailImageDescription</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="9e8ee-1529">Cadeia de caracteres terminada em nulo que especifica o título da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="9e8ee-1530">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1530">Property info</span></span> | <span data-ttu-id="9e8ee-1531">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1532">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1532">Tag</span></span>   | <span data-ttu-id="9e8ee-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1533">0x5025</span></span>                                             |
| <span data-ttu-id="9e8ee-1534">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1534">Type</span></span>  | <span data-ttu-id="9e8ee-1535">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1536">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1536">Count</span></span> | <span data-ttu-id="9e8ee-1537">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="9e8ee-1538">PropertyTagThumbnailEquipMake</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="9e8ee-1539">Cadeia de caracteres terminada em nulo que especifica o fabricante do equipamento usado para gravar a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1540">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1540">Property info</span></span> | <span data-ttu-id="9e8ee-1541">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1542">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1542">Tag</span></span>   | <span data-ttu-id="9e8ee-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1543">0x5026</span></span>                                             |
| <span data-ttu-id="9e8ee-1544">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1544">Type</span></span>  | <span data-ttu-id="9e8ee-1545">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1546">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1546">Count</span></span> | <span data-ttu-id="9e8ee-1547">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="9e8ee-1548">PropertyTagThumbnailEquipModel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="9e8ee-1549">Cadeia de caracteres terminada em nulo que especifica o nome do modelo ou o número do modelo do equipamento usado para gravar a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1550">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1550">Property info</span></span> | <span data-ttu-id="9e8ee-1551">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1552">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1552">Tag</span></span>   | <span data-ttu-id="9e8ee-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1553">0x5027</span></span>                                             |
| <span data-ttu-id="9e8ee-1554">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1554">Type</span></span>  | <span data-ttu-id="9e8ee-1555">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1556">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1556">Count</span></span> | <span data-ttu-id="9e8ee-1557">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="9e8ee-1558">PropertyTagThumbnailStripOffsets</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="9e8ee-1559">Para cada faixa na imagem em miniatura, o deslocamento de bytes dessa faixa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="9e8ee-1560">Consulte também [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) e [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="9e8ee-1561">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1561">Property info</span></span> | <span data-ttu-id="9e8ee-1562">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-1563">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1563">Tag</span></span>   | <span data-ttu-id="9e8ee-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1564">0x5028</span></span>                                      |
| <span data-ttu-id="9e8ee-1565">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1565">Type</span></span>  | <span data-ttu-id="9e8ee-1566">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1567">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1567">Count</span></span> | <span data-ttu-id="9e8ee-1568">Número de faixas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="9e8ee-1569">PropertyTagThumbnailOrientation</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="9e8ee-1570">Orientação da imagem em miniatura em termos de linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="9e8ee-1571">Consulte também [PropertyTagOrientation](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="9e8ee-1572">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1572">Property info</span></span> | <span data-ttu-id="9e8ee-1573">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1574">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1574">Tag</span></span>   | <span data-ttu-id="9e8ee-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1575">0x5029</span></span>               |
| <span data-ttu-id="9e8ee-1576">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1576">Type</span></span>  | <span data-ttu-id="9e8ee-1577">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1578">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1578">Count</span></span> | <span data-ttu-id="9e8ee-1579">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="9e8ee-1580">PropertyTagThumbnailSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="9e8ee-1581">Número de componentes de cor por pixel na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1582">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1582">Property info</span></span> | <span data-ttu-id="9e8ee-1583">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1584">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1584">Tag</span></span>   | <span data-ttu-id="9e8ee-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1585">0x502A</span></span>               |
| <span data-ttu-id="9e8ee-1586">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1586">Type</span></span>  | <span data-ttu-id="9e8ee-1587">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1588">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1588">Count</span></span> | <span data-ttu-id="9e8ee-1589">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="9e8ee-1590">PropertyTagThumbnailRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="9e8ee-1591">Número de linhas por faixa na imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1592">Consulte também [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) e [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="9e8ee-1593">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1593">Property info</span></span> | <span data-ttu-id="9e8ee-1594">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-1595">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1595">Tag</span></span>   | <span data-ttu-id="9e8ee-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1596">0x502B</span></span>                                      |
| <span data-ttu-id="9e8ee-1597">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1597">Type</span></span>  | <span data-ttu-id="9e8ee-1598">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1599">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1599">Count</span></span> | <span data-ttu-id="9e8ee-1600">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="9e8ee-1601">PropertyTagThumbnailStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="9e8ee-1602">Para cada faixa de imagem em miniatura, o número total de bytes nessa faixa.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="9e8ee-1603">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1603">Property info</span></span> | <span data-ttu-id="9e8ee-1604">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-1605">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1605">Tag</span></span>   | <span data-ttu-id="9e8ee-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1606">0x502C</span></span>                                      |
| <span data-ttu-id="9e8ee-1607">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1607">Type</span></span>  | <span data-ttu-id="9e8ee-1608">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1609">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1609">Count</span></span> | <span data-ttu-id="9e8ee-1610">Número de faixas na imagem em miniatura</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="9e8ee-1611">PropertyTagThumbnailResolutionX</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="9e8ee-1612">Resolução de miniaturas na direção da largura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="9e8ee-1613">A unidade de resolução é fornecida em [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-1614">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1614">Property info</span></span> | <span data-ttu-id="9e8ee-1615">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="9e8ee-1616">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1616">Tag</span></span> | <span data-ttu-id="9e8ee-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="9e8ee-1618">PropertyTagThumbnailResolutionY</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="9e8ee-1619">Resolução de miniaturas na direção da altura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="9e8ee-1620">A unidade de resolução é fornecida em [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-1621">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1621">Property info</span></span> | <span data-ttu-id="9e8ee-1622">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="9e8ee-1623">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1623">Tag</span></span> | <span data-ttu-id="9e8ee-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="9e8ee-1625">PropertyTagThumbnailPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="9e8ee-1626">Se os componentes de pixel na imagem em miniatura são registrados no formato de partes ou do planar.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="9e8ee-1627">Consulte também [PropertyTagPlanarConfig](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="9e8ee-1628">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1628">Property info</span></span> | <span data-ttu-id="9e8ee-1629">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1630">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1630">Tag</span></span>   | <span data-ttu-id="9e8ee-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1631">0x502F</span></span>               |
| <span data-ttu-id="9e8ee-1632">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1632">Type</span></span>  | <span data-ttu-id="9e8ee-1633">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1634">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1634">Count</span></span> | <span data-ttu-id="9e8ee-1635">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="9e8ee-1636">PropertyTagThumbnailResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="9e8ee-1637">Unidade de medida para a resolução horizontal e a resolução vertical da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1638">Consulte também [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="9e8ee-1639">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1639">Property info</span></span> | <span data-ttu-id="9e8ee-1640">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1641">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1641">Tag</span></span>   | <span data-ttu-id="9e8ee-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1642">0x5030</span></span>               |
| <span data-ttu-id="9e8ee-1643">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1643">Type</span></span>  | <span data-ttu-id="9e8ee-1644">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1645">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1645">Count</span></span> | <span data-ttu-id="9e8ee-1646">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="9e8ee-1647">PropertyTagThumbnailTransferFunction</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="9e8ee-1648">Tabelas que especificam funções de transferência para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1649">Consulte também [PropertyTagTransferFunction](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="9e8ee-1650">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1650">Property info</span></span> | <span data-ttu-id="9e8ee-1651">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="9e8ee-1652">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1652">Tag</span></span>   | <span data-ttu-id="9e8ee-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1653">0x5031</span></span>                                               |
| <span data-ttu-id="9e8ee-1654">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1654">Type</span></span>  | <span data-ttu-id="9e8ee-1655">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="9e8ee-1656">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1656">Count</span></span> | <span data-ttu-id="9e8ee-1657">Número total de palavras de 16 bits necessárias para as tabelas</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="9e8ee-1658">PropertyTagThumbnailSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="9e8ee-1659">Cadeia de caracteres terminada em nulo que especifica o nome e a versão do software ou firmware do dispositivo usado para gerar a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1660">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1660">Property info</span></span> | <span data-ttu-id="9e8ee-1661">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1662">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1662">Tag</span></span>   | <span data-ttu-id="9e8ee-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1663">0x5032</span></span>                                             |
| <span data-ttu-id="9e8ee-1664">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1664">Type</span></span>  | <span data-ttu-id="9e8ee-1665">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1666">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1666">Count</span></span> | <span data-ttu-id="9e8ee-1667">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="9e8ee-1668">PropertyTagThumbnailDateTime</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="9e8ee-1669">Data e hora em que a imagem em miniatura foi criada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="9e8ee-1670">Consulte também [PropertyTagDateTime](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="9e8ee-1671">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1671">Property info</span></span> | <span data-ttu-id="9e8ee-1672">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1673">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1673">Tag</span></span>   | <span data-ttu-id="9e8ee-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1674">0x5033</span></span>               |
| <span data-ttu-id="9e8ee-1675">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1675">Type</span></span>  | <span data-ttu-id="9e8ee-1676">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-1677">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1677">Count</span></span> | <span data-ttu-id="9e8ee-1678">20</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="9e8ee-1679">PropertyTagThumbnailArtist</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="9e8ee-1680">Cadeia de caracteres terminada em nulo que especifica o nome da pessoa que criou a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1681">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1681">Property info</span></span> | <span data-ttu-id="9e8ee-1682">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1683">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1683">Tag</span></span>   | <span data-ttu-id="9e8ee-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1684">0x5034</span></span>                                             |
| <span data-ttu-id="9e8ee-1685">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1685">Type</span></span>  | <span data-ttu-id="9e8ee-1686">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1687">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1687">Count</span></span> | <span data-ttu-id="9e8ee-1688">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="9e8ee-1689">PropertyTagThumbnailWhitePoint</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="9e8ee-1690">A desvio do ponto branco da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1691">Consulte também [PropertyTagWhitePoint](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="9e8ee-1692">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1692">Property info</span></span> | <span data-ttu-id="9e8ee-1693">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1694">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1694">Tag</span></span>   | <span data-ttu-id="9e8ee-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1695">0x5035</span></span>                  |
| <span data-ttu-id="9e8ee-1696">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1696">Type</span></span>  | <span data-ttu-id="9e8ee-1697">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1698">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1698">Count</span></span> | <span data-ttu-id="9e8ee-1699">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="9e8ee-1700">PropertyTagThumbnailPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="9e8ee-1701">Para cada uma das três cores primárias na imagem em miniatura, a desvio dessa cor.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="9e8ee-1702">Consulte também [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="9e8ee-1703">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1703">Property info</span></span> | <span data-ttu-id="9e8ee-1704">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1705">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1705">Tag</span></span>   | <span data-ttu-id="9e8ee-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1706">0x5036</span></span>                  |
| <span data-ttu-id="9e8ee-1707">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1707">Type</span></span>  | <span data-ttu-id="9e8ee-1708">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1709">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1709">Count</span></span> | <span data-ttu-id="9e8ee-1710">6</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="9e8ee-1711">PropertyTagThumbnailYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="9e8ee-1712">Coeficientes para transformação de RGB para dados YCbCr para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1713">Consulte também [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="9e8ee-1714">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1714">Property info</span></span> | <span data-ttu-id="9e8ee-1715">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1716">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1716">Tag</span></span>   | <span data-ttu-id="9e8ee-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1717">0x5037</span></span>                  |
| <span data-ttu-id="9e8ee-1718">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1718">Type</span></span>  | <span data-ttu-id="9e8ee-1719">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1720">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1720">Count</span></span> | <span data-ttu-id="9e8ee-1721">3</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="9e8ee-1722">PropertyTagThumbnailYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="9e8ee-1723">Taxa de amostragem de componentes crominância em relação ao componente de luminância para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1724">Consulte também [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="9e8ee-1725">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1725">Property info</span></span> | <span data-ttu-id="9e8ee-1726">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1727">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1727">Tag</span></span>   | <span data-ttu-id="9e8ee-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1728">0x5038</span></span>               |
| <span data-ttu-id="9e8ee-1729">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1729">Type</span></span>  | <span data-ttu-id="9e8ee-1730">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1731">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1731">Count</span></span> | <span data-ttu-id="9e8ee-1732">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="9e8ee-1733">PropertyTagThumbnailYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="9e8ee-1734">Posição dos componentes crominância em relação ao componente de luminância para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1735">Consulte também [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="9e8ee-1736">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1736">Property info</span></span> | <span data-ttu-id="9e8ee-1737">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1738">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1738">Tag</span></span>   | <span data-ttu-id="9e8ee-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1739">0x5039</span></span>               |
| <span data-ttu-id="9e8ee-1740">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1740">Type</span></span>  | <span data-ttu-id="9e8ee-1741">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1742">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1742">Count</span></span> | <span data-ttu-id="9e8ee-1743">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="9e8ee-1744">PropertyTagThumbnailRefBlackWhite</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="9e8ee-1745">Valor de ponto preto de referência e valor de ponto branco de referência para a imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="9e8ee-1746">Consulte também [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="9e8ee-1747">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1747">Property info</span></span> | <span data-ttu-id="9e8ee-1748">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1749">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1749">Tag</span></span>   | <span data-ttu-id="9e8ee-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1750">0x503A</span></span>                  |
| <span data-ttu-id="9e8ee-1751">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1751">Type</span></span>  | <span data-ttu-id="9e8ee-1752">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1753">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1753">Count</span></span> | <span data-ttu-id="9e8ee-1754">6</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="9e8ee-1755">PropertyTagThumbnailCopyRight</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="9e8ee-1756">Cadeia de caracteres terminada em nulo que contém informações de direitos autorais da imagem em miniatura.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="9e8ee-1757">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1757">Property info</span></span> | <span data-ttu-id="9e8ee-1758">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1759">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1759">Tag</span></span>   | <span data-ttu-id="9e8ee-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1760">0x503B</span></span>                                             |
| <span data-ttu-id="9e8ee-1761">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1761">Type</span></span>  | <span data-ttu-id="9e8ee-1762">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1763">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1763">Count</span></span> | <span data-ttu-id="9e8ee-1764">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="9e8ee-1765">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="9e8ee-1766">Tabela de luminância.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1766">Luminance table.</span></span> <span data-ttu-id="9e8ee-1767">A tabela de luminescência e a tabela crominância são usadas para controlar a qualidade JPEG.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="9e8ee-1768">Uma tabela de luminância ou crominância válida tem 64 entradas do tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="9e8ee-1769">Se uma imagem tiver uma tabela de luminância ou uma tabela crominância, ela deverá ter ambas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="9e8ee-1770">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1770">Property info</span></span> | <span data-ttu-id="9e8ee-1771">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1772">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1772">Tag</span></span>   | <span data-ttu-id="9e8ee-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1773">0x5090</span></span>               |
| <span data-ttu-id="9e8ee-1774">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1774">Type</span></span>  | <span data-ttu-id="9e8ee-1775">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1776">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1776">Count</span></span> | <span data-ttu-id="9e8ee-1777">64</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="9e8ee-1778">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="9e8ee-1779">Tabela crominância.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1779">Chrominance table.</span></span> <span data-ttu-id="9e8ee-1780">A tabela de luminescência e a tabela crominância são usadas para controlar a qualidade JPEG.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="9e8ee-1781">Uma tabela de luminância ou crominância válida tem 64 entradas do tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="9e8ee-1782">Se uma imagem tiver uma tabela de luminância ou uma tabela crominância, ela deverá ter ambas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="9e8ee-1783">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1783">Property info</span></span> | <span data-ttu-id="9e8ee-1784">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1785">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1785">Tag</span></span>   | <span data-ttu-id="9e8ee-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1786">0x5091</span></span>               |
| <span data-ttu-id="9e8ee-1787">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1787">Type</span></span>  | <span data-ttu-id="9e8ee-1788">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1789">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1789">Count</span></span> | <span data-ttu-id="9e8ee-1790">64</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="9e8ee-1791">PropertyTagFrameDelay</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="9e8ee-1792">Tempo de atraso, em centésimos de um segundo, entre dois quadros em uma imagem GIF animada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="9e8ee-1793">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1793">Property info</span></span> | <span data-ttu-id="9e8ee-1794">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="9e8ee-1795">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1795">Tag</span></span>   | <span data-ttu-id="9e8ee-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1796">0x5100</span></span>                        |
| <span data-ttu-id="9e8ee-1797">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1797">Type</span></span>  | <span data-ttu-id="9e8ee-1798">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="9e8ee-1799">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1799">Count</span></span> | <span data-ttu-id="9e8ee-1800">Número de quadros na imagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="9e8ee-1801">PropertyTagLoopCount</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="9e8ee-1802">Para uma imagem GIF animada, o número de vezes para exibir a animação.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="9e8ee-1803">Um valor de 0 especifica que a animação deve ser exibida infinitamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="9e8ee-1804">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1804">Property info</span></span> | <span data-ttu-id="9e8ee-1805">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1806">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1806">Tag</span></span>   | <span data-ttu-id="9e8ee-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1807">0x5101</span></span>               |
| <span data-ttu-id="9e8ee-1808">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1808">Type</span></span>  | <span data-ttu-id="9e8ee-1809">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1810">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1810">Count</span></span> | <span data-ttu-id="9e8ee-1811">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="9e8ee-1812">PropertyTagGlobalPalette</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="9e8ee-1813">Paleta de cores para um bitmap indexado em uma imagem GIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="9e8ee-1814">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1814">Property info</span></span> | <span data-ttu-id="9e8ee-1815">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="9e8ee-1816">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1816">Tag</span></span>   | <span data-ttu-id="9e8ee-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1817">0x5102</span></span>                        |
| <span data-ttu-id="9e8ee-1818">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1818">Type</span></span>  | <span data-ttu-id="9e8ee-1819">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="9e8ee-1820">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1820">Count</span></span> | <span data-ttu-id="9e8ee-1821">3 x número de entradas da paleta</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="9e8ee-1822">PropertyTagIndexBackground</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="9e8ee-1823">Índice da cor do plano de fundo na paleta de uma imagem GIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="9e8ee-1824">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1824">Property info</span></span> | <span data-ttu-id="9e8ee-1825">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1826">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1826">Tag</span></span>   | <span data-ttu-id="9e8ee-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1827">0x5103</span></span>              |
| <span data-ttu-id="9e8ee-1828">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1828">Type</span></span>  | <span data-ttu-id="9e8ee-1829">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-1830">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1830">Count</span></span> | <span data-ttu-id="9e8ee-1831">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="9e8ee-1832">PropertyTagIndexTransparent</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="9e8ee-1833">Índice da cor transparente na paleta de uma imagem GIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="9e8ee-1834">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1834">Property info</span></span> | <span data-ttu-id="9e8ee-1835">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1836">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1836">Tag</span></span>   | <span data-ttu-id="9e8ee-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1837">0x5104</span></span>              |
| <span data-ttu-id="9e8ee-1838">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1838">Type</span></span>  | <span data-ttu-id="9e8ee-1839">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="9e8ee-1840">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1840">Count</span></span> | <span data-ttu-id="9e8ee-1841">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="9e8ee-1842">PropertyTagPixelUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="9e8ee-1843">Unidade para PropertyTagPixelPerUnitX e PropertyTagPixelPerUnitY.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="9e8ee-1844">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1844">Tag</span></span>

<span data-ttu-id="9e8ee-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1845">0x5110</span></span>

<span data-ttu-id="9e8ee-1846">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1846">Type</span></span>

<span data-ttu-id="9e8ee-1847">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="9e8ee-1848">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1848">Count</span></span>

<span data-ttu-id="9e8ee-1849">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1849">1</span></span>

<span data-ttu-id="9e8ee-1850">0-desconhecido</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="9e8ee-1851">PropertyTagPixelPerUnitX</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="9e8ee-1852">Pixels por unidade na direção x.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="9e8ee-1853">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1853">Property info</span></span> | <span data-ttu-id="9e8ee-1854">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1855">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1855">Tag</span></span>   | <span data-ttu-id="9e8ee-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1856">0x5111</span></span>              |
| <span data-ttu-id="9e8ee-1857">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1857">Type</span></span>  | <span data-ttu-id="9e8ee-1858">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1859">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1859">Count</span></span> | <span data-ttu-id="9e8ee-1860">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="9e8ee-1861">PropertyTagPixelPerUnitY</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="9e8ee-1862">Pixels por unidade na direção y.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="9e8ee-1863">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1863">Property info</span></span> | <span data-ttu-id="9e8ee-1864">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1865">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1865">Tag</span></span>   | <span data-ttu-id="9e8ee-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1866">0x5112</span></span>              |
| <span data-ttu-id="9e8ee-1867">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1867">Type</span></span>  | <span data-ttu-id="9e8ee-1868">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1869">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1869">Count</span></span> | <span data-ttu-id="9e8ee-1870">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="9e8ee-1871">PropertyTagPaletteHistogram</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="9e8ee-1872">Histograma da paleta.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1872">Palette histogram.</span></span>



| <span data-ttu-id="9e8ee-1873">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1873">Property info</span></span> | <span data-ttu-id="9e8ee-1874">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1875">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1875">Tag</span></span>   | <span data-ttu-id="9e8ee-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1876">0x5113</span></span>                  |
| <span data-ttu-id="9e8ee-1877">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1877">Type</span></span>  | <span data-ttu-id="9e8ee-1878">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="9e8ee-1879">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1879">Count</span></span> | <span data-ttu-id="9e8ee-1880">Comprimento do histograma</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="9e8ee-1881">PropertyTagCopyright</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="9e8ee-1882">Cadeia de caracteres terminada em nulo que contém informações de direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="9e8ee-1883">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1883">Property info</span></span> | <span data-ttu-id="9e8ee-1884">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1885">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1885">Tag</span></span>   | <span data-ttu-id="9e8ee-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1886">0x8298</span></span>                                             |
| <span data-ttu-id="9e8ee-1887">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1887">Type</span></span>  | <span data-ttu-id="9e8ee-1888">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1889">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1889">Count</span></span> | <span data-ttu-id="9e8ee-1890">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="9e8ee-1891">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="9e8ee-1892">Tempo de exposição, medido em segundos.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="9e8ee-1893">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1893">Property info</span></span> | <span data-ttu-id="9e8ee-1894">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-1895">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1895">Tag</span></span>   | <span data-ttu-id="9e8ee-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1896">0x829A</span></span>                  |
| <span data-ttu-id="9e8ee-1897">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1897">Type</span></span>  | <span data-ttu-id="9e8ee-1898">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-1899">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1899">Count</span></span> | <span data-ttu-id="9e8ee-1900">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="9e8ee-1901">PropertyTagExifFNumber</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="9e8ee-1902">Número F.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1902">F number.</span></span>



| <span data-ttu-id="9e8ee-1903">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1903">Property info</span></span> | <span data-ttu-id="9e8ee-1904">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="9e8ee-1905">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1905">Tag</span></span>   | <span data-ttu-id="9e8ee-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1906">0x829D</span></span>   |
| <span data-ttu-id="9e8ee-1907">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1907">Type</span></span>  | <span data-ttu-id="9e8ee-1908">RACIONAL</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1908">RATIONAL</span></span> |
| <span data-ttu-id="9e8ee-1909">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1909">Count</span></span> | <span data-ttu-id="9e8ee-1910">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="9e8ee-1911">PropertyTagExifIFD</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="9e8ee-1912">Marca particular usada pelo GDI+.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="9e8ee-1913">Não destinado ao uso público.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1913">Not for public use.</span></span> <span data-ttu-id="9e8ee-1914">O GDI+ usa essa marca para localizar informações específicas de EXIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="9e8ee-1915">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1915">Property info</span></span> | <span data-ttu-id="9e8ee-1916">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1917">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1917">Tag</span></span>   | <span data-ttu-id="9e8ee-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1918">0x8769</span></span>              |
| <span data-ttu-id="9e8ee-1919">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1919">Type</span></span>  | <span data-ttu-id="9e8ee-1920">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1921">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1921">Count</span></span> | <span data-ttu-id="9e8ee-1922">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="9e8ee-1923">PropertyTagICCProfile</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="9e8ee-1924">Perfil ICC inserido na imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="9e8ee-1925">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1925">Property info</span></span> | <span data-ttu-id="9e8ee-1926">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="9e8ee-1927">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1927">Tag</span></span>   | <span data-ttu-id="9e8ee-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1928">0x8773</span></span>                |
| <span data-ttu-id="9e8ee-1929">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1929">Type</span></span>  | <span data-ttu-id="9e8ee-1930">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="9e8ee-1931">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1931">Count</span></span> | <span data-ttu-id="9e8ee-1932">Comprimento do perfil</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="9e8ee-1933">PropertyTagExifExposureProg</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="9e8ee-1934">Classe do programa usada pela câmera para definir a exposição quando a imagem é executada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="9e8ee-1935">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1935">Tag</span></span>

<span data-ttu-id="9e8ee-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1936">0x8822</span></span>

<span data-ttu-id="9e8ee-1937">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1937">Type</span></span>

<span data-ttu-id="9e8ee-1938">BAIXO</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1938">SHORT</span></span>

<span data-ttu-id="9e8ee-1939">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1939">Count</span></span>

<span data-ttu-id="9e8ee-1940">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1940">1</span></span>

<span data-ttu-id="9e8ee-1941">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1941">Default</span></span>

<span data-ttu-id="9e8ee-1942">0</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1942">0</span></span>

<span data-ttu-id="9e8ee-1943">0-não definido 1-Manual 2-programa normal 3-prioridade de abertura 4-prioridade 5 do obturador – programa criativo (em relação à profundidade do campo) 6-programa de ação (polarizado em direção à rapidez velocidade do obturador) 7-modo retrato (para fotos de fechamento com o plano de fundo fora do foco) modo 8-paisagem (para fotos em paisagem com o plano de fundo em foco) de 9 a 255-reservado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="9e8ee-1944">PropertyTagExifSpectralSense</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="9e8ee-1945">Cadeia de caracteres terminada em nulo que especifica a sensibilidade de Spectral de cada canal da câmera usada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="9e8ee-1946">A cadeia de caracteres é compatível com o padrão desenvolvido pelo comitê técnico do ASTM.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="9e8ee-1947">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1947">Property info</span></span> | <span data-ttu-id="9e8ee-1948">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-1949">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1949">Tag</span></span>   | <span data-ttu-id="9e8ee-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1950">0x8824</span></span>                                             |
| <span data-ttu-id="9e8ee-1951">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1951">Type</span></span>  | <span data-ttu-id="9e8ee-1952">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-1953">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1953">Count</span></span> | <span data-ttu-id="9e8ee-1954">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="9e8ee-1955">PropertyTagGpsIFD</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="9e8ee-1956">Deslocamento para um bloco de itens de propriedade GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="9e8ee-1957">Itens de propriedade cujas marcas têm o prefixo PropertyTagGps são armazenadas no bloco GPS.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="9e8ee-1958">Os itens de propriedade GPS são definidos na especificação EXIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="9e8ee-1959">O GDI+ usa essa marca para localizar informações de GPS, mas GDI+ não expõe essa marca para uso público.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="9e8ee-1960">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1960">Property info</span></span> | <span data-ttu-id="9e8ee-1961">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-1962">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1962">Tag</span></span>   | <span data-ttu-id="9e8ee-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1963">0x8825</span></span>              |
| <span data-ttu-id="9e8ee-1964">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1964">Type</span></span>  | <span data-ttu-id="9e8ee-1965">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-1966">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1966">Count</span></span> | <span data-ttu-id="9e8ee-1967">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="9e8ee-1968">PropertyTagExifISOSpeed</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="9e8ee-1969">Velocidade ISO e latitude ISO da câmera ou dispositivo de entrada, conforme especificado no ISO 12232.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="9e8ee-1970">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1970">Property info</span></span> | <span data-ttu-id="9e8ee-1971">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-1972">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1972">Tag</span></span>   | <span data-ttu-id="9e8ee-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1973">0x8827</span></span>               |
| <span data-ttu-id="9e8ee-1974">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1974">Type</span></span>  | <span data-ttu-id="9e8ee-1975">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-1976">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1976">Count</span></span> | <span data-ttu-id="9e8ee-1977">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="9e8ee-1978">PropertyTagExifOECF</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="9e8ee-1979">Função de conversão Optoelectronic (OECF) especificada no ISO 14524.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="9e8ee-1980">O OECF é a relação entre a entrada óptica da câmera e os valores da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="9e8ee-1981">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1981">Property info</span></span> | <span data-ttu-id="9e8ee-1982">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-1983">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1983">Tag</span></span>   | <span data-ttu-id="9e8ee-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1984">0x8828</span></span>                   |
| <span data-ttu-id="9e8ee-1985">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1985">Type</span></span>  | <span data-ttu-id="9e8ee-1986">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-1987">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1987">Count</span></span> | <span data-ttu-id="9e8ee-1988">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="9e8ee-1989">PropertyTagExifVer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="9e8ee-1990">Versão do padrão de EXIF com suporte.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="9e8ee-1991">A não existência deste campo é usada para significar não conformidade com o padrão.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="9e8ee-1992">A conformidade com o padrão é indicada pela gravação de 0210 como uma cadeia de caracteres ASCII de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="9e8ee-1993">Como o tipo é PropertyTagTypeUndefined, não há nenhum terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="9e8ee-1994">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1994">Property info</span></span> | <span data-ttu-id="9e8ee-1995">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="9e8ee-1996">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1996">Tag</span></span>     | <span data-ttu-id="9e8ee-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1997">0x9000</span></span>                   |
| <span data-ttu-id="9e8ee-1998">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1998">Type</span></span>    | <span data-ttu-id="9e8ee-1999">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2000">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2000">Count</span></span>   | <span data-ttu-id="9e8ee-2001">4</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2001">4</span></span>                        |
| <span data-ttu-id="9e8ee-2002">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2002">Default</span></span> | <span data-ttu-id="9e8ee-2003">0210</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="9e8ee-2004">PropertyTagExifDTOrig</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="9e8ee-2005">Data e hora em que os dados da imagem original foram gerados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="9e8ee-2006">Para uma DSC, a data e a hora em que a imagem foi tirada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="9e8ee-2007">O formato é aaaa: MM: DD HH: MM: SS com o tempo mostrado no formato de 24 horas e a data e hora separadas por um caractere em branco (0x2000).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="9e8ee-2008">O comprimento da cadeia de caracteres é de 20 bytes, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="9e8ee-2009">Quando o campo está vazio, ele é tratado como desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="9e8ee-2010">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2010">Property info</span></span> | <span data-ttu-id="9e8ee-2011">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-2012">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2012">Tag</span></span>   | <span data-ttu-id="9e8ee-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2013">0x9003</span></span>               |
| <span data-ttu-id="9e8ee-2014">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2014">Type</span></span>  | <span data-ttu-id="9e8ee-2015">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-2016">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2016">Count</span></span> | <span data-ttu-id="9e8ee-2017">20</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="9e8ee-2018">PropertyTagExifDTDigitized</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="9e8ee-2019">Data e hora em que a imagem foi armazenada como dados digitais.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="9e8ee-2020">Se, por exemplo, uma imagem foi capturada pela DSC e, ao mesmo tempo em que o arquivo foi gravado, DateTimeOriginal e DateTimeDigitized terão o mesmo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="9e8ee-2021">O formato é aaaa: MM: DD HH: MM: SS com o tempo mostrado no formato de 24 horas e a data e hora separadas por um caractere em branco (0x2000).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="9e8ee-2022">O comprimento da cadeia de caracteres é de 20 bytes, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="9e8ee-2023">Quando o campo está vazio, ele é tratado como desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="9e8ee-2024">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2024">Property info</span></span> | <span data-ttu-id="9e8ee-2025">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-2026">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2026">Tag</span></span>   | <span data-ttu-id="9e8ee-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2027">0x9004</span></span>               |
| <span data-ttu-id="9e8ee-2028">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2028">Type</span></span>  | <span data-ttu-id="9e8ee-2029">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-2030">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2030">Count</span></span> | <span data-ttu-id="9e8ee-2031">20</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="9e8ee-2032">PropertyTagExifCompConfig</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="9e8ee-2033">Informações específicas para dados compactados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2033">Information specific to compressed data.</span></span> <span data-ttu-id="9e8ee-2034">Os canais de cada componente são organizados em ordem do primeiro componente até o quarto.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="9e8ee-2035">Para dados descompactados, a disposição dos dados é fornecida na marca PropertyTagPhotometricInterp.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="9e8ee-2036">No entanto, como PropertyTagPhotometricInterp só pode expressar a ordem de Y, CB e CR, essa marca é fornecida para casos em que os dados compactados usam componentes diferentes de Y, CB e CR e para dar suporte a outras sequências.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="9e8ee-2037">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2037">Tag</span></span>

<span data-ttu-id="9e8ee-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2038">0x9101</span></span>

<span data-ttu-id="9e8ee-2039">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2039">Type</span></span>

<span data-ttu-id="9e8ee-2040">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="9e8ee-2041">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2041">Count</span></span>

<span data-ttu-id="9e8ee-2042">4</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2042">4</span></span>

<span data-ttu-id="9e8ee-2043">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2043">Default</span></span>

<span data-ttu-id="9e8ee-2044">4 5 6 0 (se RGB descompactado) 1 2 3 0 (outros casos)</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="9e8ee-2045">0-não existe 1-Y 2-CB 3-CR 4-R 5-G 6-B Other-reserved</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="9e8ee-2046">PropertyTagExifCompBPP</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="9e8ee-2047">Informações específicas para dados compactados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2047">Information specific to compressed data.</span></span> <span data-ttu-id="9e8ee-2048">O modo de compactação usado para uma imagem compactada é indicado na unidade BPP.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="9e8ee-2049">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2049">Property info</span></span> | <span data-ttu-id="9e8ee-2050">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2051">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2051">Tag</span></span>   | <span data-ttu-id="9e8ee-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2052">0x9102</span></span>                  |
| <span data-ttu-id="9e8ee-2053">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2053">Type</span></span>  | <span data-ttu-id="9e8ee-2054">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2055">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2055">Count</span></span> | <span data-ttu-id="9e8ee-2056">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="9e8ee-2057">PropertyTagExifShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="9e8ee-2058">Velocidade do obturador.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2058">Shutter speed.</span></span> <span data-ttu-id="9e8ee-2059">A unidade é o sistema aditivo de valor de exposição fotográfica (APEX).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="9e8ee-2060">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2060">Property info</span></span> | <span data-ttu-id="9e8ee-2061">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2062">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2062">Tag</span></span>   | <span data-ttu-id="9e8ee-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2063">0x9201</span></span>                   |
| <span data-ttu-id="9e8ee-2064">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2064">Type</span></span>  | <span data-ttu-id="9e8ee-2065">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="9e8ee-2066">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2066">Count</span></span> | <span data-ttu-id="9e8ee-2067">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="9e8ee-2068">PropertyTagExifAperture</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="9e8ee-2069">Abertura de lentes.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2069">Lens aperture.</span></span> <span data-ttu-id="9e8ee-2070">A unidade é o valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="9e8ee-2071">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2071">Property info</span></span> | <span data-ttu-id="9e8ee-2072">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2073">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2073">Tag</span></span>   | <span data-ttu-id="9e8ee-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2074">0x9202</span></span>                  |
| <span data-ttu-id="9e8ee-2075">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2075">Type</span></span>  | <span data-ttu-id="9e8ee-2076">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2077">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2077">Count</span></span> | <span data-ttu-id="9e8ee-2078">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="9e8ee-2079">PropertyTagExifBrightness</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="9e8ee-2080">Valor de brilho.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2080">Brightness value.</span></span> <span data-ttu-id="9e8ee-2081">A unidade é o valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2081">The unit is the APEX value.</span></span> <span data-ttu-id="9e8ee-2082">Normalmente, ele é fornecido no intervalo de-99,99 a 99,99.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="9e8ee-2083">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2083">Property info</span></span> | <span data-ttu-id="9e8ee-2084">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2085">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2085">Tag</span></span>   | <span data-ttu-id="9e8ee-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2086">0x9203</span></span>                   |
| <span data-ttu-id="9e8ee-2087">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2087">Type</span></span>  | <span data-ttu-id="9e8ee-2088">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="9e8ee-2089">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2089">Count</span></span> | <span data-ttu-id="9e8ee-2090">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="9e8ee-2091">PropertyTagExifExposureBias</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="9e8ee-2092">Tendência de exposição.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2092">Exposure bias.</span></span> <span data-ttu-id="9e8ee-2093">A unidade é o valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2093">The unit is the APEX value.</span></span> <span data-ttu-id="9e8ee-2094">Normalmente, ele é fornecido no intervalo de-99,99 a 99,99.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="9e8ee-2095">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2095">Property info</span></span> | <span data-ttu-id="9e8ee-2096">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2097">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2097">Tag</span></span>   | <span data-ttu-id="9e8ee-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2098">0x9204</span></span>                   |
| <span data-ttu-id="9e8ee-2099">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2099">Type</span></span>  | <span data-ttu-id="9e8ee-2100">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="9e8ee-2101">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2101">Count</span></span> | <span data-ttu-id="9e8ee-2102">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="9e8ee-2103">PropertyTagExifMaxAperture</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="9e8ee-2104">Menor número F da lente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="9e8ee-2105">A unidade é o valor de APEX.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2105">The unit is the APEX value.</span></span> <span data-ttu-id="9e8ee-2106">Normalmente, ele é fornecido no intervalo de 0, 0 a 99,99, mas não está limitado a esse intervalo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="9e8ee-2107">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2107">Property info</span></span> | <span data-ttu-id="9e8ee-2108">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2109">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2109">Tag</span></span>   | <span data-ttu-id="9e8ee-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2110">0x9205</span></span>                  |
| <span data-ttu-id="9e8ee-2111">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2111">Type</span></span>  | <span data-ttu-id="9e8ee-2112">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2113">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2113">Count</span></span> | <span data-ttu-id="9e8ee-2114">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="9e8ee-2115">PropertyTagExifSubjectDist</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="9e8ee-2116">Distância para o assunto, medida em metros.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="9e8ee-2117">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2117">Property info</span></span> | <span data-ttu-id="9e8ee-2118">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2119">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2119">Tag</span></span>   | <span data-ttu-id="9e8ee-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2120">0x9206</span></span>                  |
| <span data-ttu-id="9e8ee-2121">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2121">Type</span></span>  | <span data-ttu-id="9e8ee-2122">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2123">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2123">Count</span></span> | <span data-ttu-id="9e8ee-2124">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="9e8ee-2125">PropertyTagExifMeteringMode</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="9e8ee-2126">Modo de medição.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2126">Metering mode.</span></span>



<span data-ttu-id="9e8ee-2127">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2127">Tag</span></span>

<span data-ttu-id="9e8ee-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2128">0x9207</span></span>

<span data-ttu-id="9e8ee-2129">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2129">Type</span></span>

<span data-ttu-id="9e8ee-2130">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2131">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2131">Count</span></span>

<span data-ttu-id="9e8ee-2132">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2132">1</span></span>

<span data-ttu-id="9e8ee-2133">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2133">Default</span></span>

<span data-ttu-id="9e8ee-2134">0</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2134">0</span></span>

<span data-ttu-id="9e8ee-2135">0-desconhecido 1-média 2-CenterWeightedAverage 3-Spot 4-AutoSpot 5-padrão 6-parcial 7 a 254-reservado 255-outro</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="9e8ee-2136">PropertyTagExifLightSource</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="9e8ee-2137">Tipo de fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2137">Type of light source.</span></span>



<span data-ttu-id="9e8ee-2138">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2138">Tag</span></span>

<span data-ttu-id="9e8ee-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2139">0x9208</span></span>

<span data-ttu-id="9e8ee-2140">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2140">Type</span></span>

<span data-ttu-id="9e8ee-2141">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2142">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2142">Count</span></span>

<span data-ttu-id="9e8ee-2143">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2143">1</span></span>

<span data-ttu-id="9e8ee-2144">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2144">Default</span></span>

<span data-ttu-id="9e8ee-2145">0</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2145">0</span></span>

<span data-ttu-id="9e8ee-2146">0-desconhecido 1-horário de verão 2-flourescent 3-Tungsten 17-luz padrão de 18-padrão Light B 19 – luz padrão C 20-D55 21-D65 22-D75 23 a 254-reservado 255-outro</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="9e8ee-2147">PropertyTagExifFlash</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="9e8ee-2148">Status do flash.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2148">Flash status.</span></span> <span data-ttu-id="9e8ee-2149">Essa marca é registrada quando uma imagem é executada usando uma luz de estroboscópico (flash).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="9e8ee-2150">O bit 0 indica o status de acionamento do flash, e os bits 1 e 2 indicam o status de retorno do flash.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="9e8ee-2151">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2151">Tag</span></span>

<span data-ttu-id="9e8ee-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2152">0x9209</span></span>

<span data-ttu-id="9e8ee-2153">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2153">Type</span></span>

<span data-ttu-id="9e8ee-2154">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2155">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2155">Count</span></span>

<span data-ttu-id="9e8ee-2156">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2156">1</span></span>

<span data-ttu-id="9e8ee-2157">Valores para o bit 0 que indicam se o flash foi acionado: 0B-flash não disparou 1B-flash acionado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="9e8ee-2158">Valores para bits 1 e 2 que indicam o status da luz retornada: 00B-nenhuma função de detecção de retorno estroboscópico 01B-reservado 10B-sinal de retorno estroboscópico não detectado 11b-luz de retorno estroboscópico detectada</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="9e8ee-2159">Valores de marca flash resultantes: 0x0000-flash não disparou 0x0001-flash disparado 0x0005-sinal de retorno estroboscópico não detectado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="9e8ee-2160">PropertyTagExifFocalLength</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="9e8ee-2161">O comprimento focal real, em milímetros, da lente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="9e8ee-2162">A conversão não é feita no comprimento focal de uma câmera de filme de 35 milímetros.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="9e8ee-2163">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2163">Property info</span></span> | <span data-ttu-id="9e8ee-2164">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2165">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2165">Tag</span></span>   | <span data-ttu-id="9e8ee-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2166">0x920A</span></span>                  |
| <span data-ttu-id="9e8ee-2167">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2167">Type</span></span>  | <span data-ttu-id="9e8ee-2168">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2169">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2169">Count</span></span> | <span data-ttu-id="9e8ee-2170">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="9e8ee-2171">PropertyTagExifMakerNote</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="9e8ee-2172">Marca de observação.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2172">Note tag.</span></span> <span data-ttu-id="9e8ee-2173">Uma marca usada pelos fabricantes de gravadores EXIF para registrar informações.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="9e8ee-2174">O conteúdo é para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="9e8ee-2175">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2175">Property info</span></span> | <span data-ttu-id="9e8ee-2176">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2177">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2177">Tag</span></span>   | <span data-ttu-id="9e8ee-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2178">0x927C</span></span>                   |
| <span data-ttu-id="9e8ee-2179">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2179">Type</span></span>  | <span data-ttu-id="9e8ee-2180">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2181">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2181">Count</span></span> | <span data-ttu-id="9e8ee-2182">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="9e8ee-2183">PropertyTagExifUserComment</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="9e8ee-2184">Marca de comentário.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2184">Comment tag.</span></span> <span data-ttu-id="9e8ee-2185">Uma marca usada por usuários do EXIF para escrever palavras-chave ou comentários sobre a imagem além daquelas em PropertyTagImageDescription e sem as limitações de código de caractere da marca PropertyTagImageDescription.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="9e8ee-2186">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2186">Property info</span></span> | <span data-ttu-id="9e8ee-2187">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2188">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2188">Tag</span></span>   | <span data-ttu-id="9e8ee-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2189">0x9286</span></span>                   |
| <span data-ttu-id="9e8ee-2190">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2190">Type</span></span>  | <span data-ttu-id="9e8ee-2191">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2192">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2192">Count</span></span> | <span data-ttu-id="9e8ee-2193">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2193">Any</span></span>                      |



 

<span data-ttu-id="9e8ee-2194">O código de caractere usado na marca PropertyTagExifUserComment é identificado com base em um código de ID em uma área fixa de 8 bytes no início da área de dados da marca.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="9e8ee-2195">A porção não utilizada da área é preenchida com caracteres nulos (0).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="9e8ee-2196">Os códigos de ID são atribuídos por meio de registro.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="9e8ee-2197">Como o tipo não é ASCII, não é necessário usar um terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="9e8ee-2198">PropertyTagExifDTSubsec</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="9e8ee-2199">Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagDateTime.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="9e8ee-2200">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2200">Property info</span></span> | <span data-ttu-id="9e8ee-2201">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-2202">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2202">Tag</span></span>   | <span data-ttu-id="9e8ee-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2203">0x9290</span></span>                                             |
| <span data-ttu-id="9e8ee-2204">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2204">Type</span></span>  | <span data-ttu-id="9e8ee-2205">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-2206">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2206">Count</span></span> | <span data-ttu-id="9e8ee-2207">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="9e8ee-2208">PropertyTagExifDTOrigSS</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="9e8ee-2209">Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagExifDTOrig.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="9e8ee-2210">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2210">Property info</span></span> | <span data-ttu-id="9e8ee-2211">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-2212">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2212">Tag</span></span>  | <span data-ttu-id="9e8ee-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2213">0x9291</span></span>                                             |
| <span data-ttu-id="9e8ee-2214">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2214">Type</span></span> | <span data-ttu-id="9e8ee-2215">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="9e8ee-2216">N</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2216">N</span></span>    | <span data-ttu-id="9e8ee-2217">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="9e8ee-2218">PropertyTagExifDTDigSS</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="9e8ee-2219">Cadeia de caracteres terminada em nulo que especifica uma fração de um segundo para a marca PropertyTagExifDTDigitized.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="9e8ee-2220">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2220">Property info</span></span> | <span data-ttu-id="9e8ee-2221">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="9e8ee-2222">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2222">Tag</span></span>  | <span data-ttu-id="9e8ee-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2223">0x9292</span></span>                                             |
| <span data-ttu-id="9e8ee-2224">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2224">Type</span></span> | <span data-ttu-id="9e8ee-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2225">ASCII</span></span>                                              |
| <span data-ttu-id="9e8ee-2226">N</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2226">N</span></span>    | <span data-ttu-id="9e8ee-2227">Comprimento da cadeia de caracteres incluindo o terminador nulo</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="9e8ee-2228">PropertyTagExifFPXVer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="9e8ee-2229">Versão de formato FlashPix com suporte por um arquivo FPXR.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="9e8ee-2230">Se a função FPXR der suporte à versão de formato FlashPix 1,0, isso será indicado da mesma forma que o PropertyTagExifVer, gravando 0100 como uma cadeia de caracteres ASCII de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="9e8ee-2231">Como o tipo é PropertyTagTypeUndefined, não há nenhum terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="9e8ee-2232">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2232">Tag</span></span>

<span data-ttu-id="9e8ee-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2233">0xA000</span></span>

<span data-ttu-id="9e8ee-2234">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2234">Type</span></span>

<span data-ttu-id="9e8ee-2235">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="9e8ee-2236">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2236">Count</span></span>

<span data-ttu-id="9e8ee-2237">4</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2237">4</span></span>

<span data-ttu-id="9e8ee-2238">Padrão</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2238">Default</span></span>

<span data-ttu-id="9e8ee-2239">0100</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2239">0100</span></span>

<span data-ttu-id="9e8ee-2240">0100-formato FlashPix versão 1,0 outro – reservado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="9e8ee-2241">PropertyTagExifColorSpace</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="9e8ee-2242">Especificador de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2242">Color space specifier.</span></span> <span data-ttu-id="9e8ee-2243">Normalmente, sRGB (= 1) é usado para definir o espaço de cores com base nas condições e no ambiente do monitor do PC.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="9e8ee-2244">Se um espaço de cores diferente de sRGB for usado, não calibrado (= 0xFFFF) será definido.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="9e8ee-2245">Os dados de imagem registrados como não calibrados podem ser tratados como sRGB quando convertidos em FlashPix.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="9e8ee-2246">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2246">Tag</span></span>

<span data-ttu-id="9e8ee-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2247">0xA001</span></span>

<span data-ttu-id="9e8ee-2248">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2248">Type</span></span>

<span data-ttu-id="9e8ee-2249">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2250">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2250">Count</span></span>

<span data-ttu-id="9e8ee-2251">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2251">1</span></span>

<span data-ttu-id="9e8ee-2252">0x1-sRGB 0xFFFF-não calibrado-reservado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="9e8ee-2253">PropertyTagExifPixXDim</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="9e8ee-2254">Informações específicas para dados compactados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2254">Information specific to compressed data.</span></span> <span data-ttu-id="9e8ee-2255">Quando um arquivo compactado é registrado, a largura válida da imagem significativa deve ser registrada nessa marca, independentemente de haver ou não dados de preenchimento ou um marcador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="9e8ee-2256">Essa marca não deve existir em um arquivo descompactado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="9e8ee-2257">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2257">Property info</span></span> | <span data-ttu-id="9e8ee-2258">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-2259">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2259">Tag</span></span>   | <span data-ttu-id="9e8ee-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2260">0xA002</span></span>                                      |
| <span data-ttu-id="9e8ee-2261">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2261">Type</span></span>  | <span data-ttu-id="9e8ee-2262">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-2263">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2263">Count</span></span> | <span data-ttu-id="9e8ee-2264">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="9e8ee-2265">PropertyTagExifPixYDim</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="9e8ee-2266">Informações específicas para dados compactados.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2266">Information specific to compressed data.</span></span> <span data-ttu-id="9e8ee-2267">Quando um arquivo compactado é registrado, a altura válida da imagem significativa deve ser registrada nessa marca se houver ou não dados de preenchimento ou um marcador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="9e8ee-2268">Essa marca não deve existir em um arquivo descompactado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="9e8ee-2269">Como o preenchimento de dados é desnecessário na direção vertical, o número de linhas registradas nessa marca de altura de imagem válida será o mesmo que o registrado no vers.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="9e8ee-2270">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2270">Property info</span></span> | <span data-ttu-id="9e8ee-2271">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="9e8ee-2272">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2272">Tag</span></span>   | <span data-ttu-id="9e8ee-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2273">0xA003</span></span>                                      |
| <span data-ttu-id="9e8ee-2274">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2274">Type</span></span>  | <span data-ttu-id="9e8ee-2275">PropertyTagTypeShort ou PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-2276">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2276">Count</span></span> | <span data-ttu-id="9e8ee-2277">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="9e8ee-2278">PropertyTagExifRelatedWav</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="9e8ee-2279">O nome de um arquivo de áudio relacionado aos dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="9e8ee-2280">As únicas informações relacionais registradas são o nome e a extensão do arquivo de áudio EXIF (uma cadeia de caracteres ASCII que consiste em 8 caracteres mais um ponto (.), mais 3 caracteres).</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="9e8ee-2281">O caminho não é registrado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2281">The path is not recorded.</span></span> <span data-ttu-id="9e8ee-2282">Quando você usa essa marca, os arquivos de áudio devem ser registrados em conformidade com o formato de áudio EXIF.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="9e8ee-2283">Os gravadores também podem armazenar dados de áudio dentro de APP2 como dados de fluxo de extensão FlashPix.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="9e8ee-2284">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2284">Property info</span></span> | <span data-ttu-id="9e8ee-2285">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-2286">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2286">Tag</span></span>   | <span data-ttu-id="9e8ee-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2287">0xA004</span></span>               |
| <span data-ttu-id="9e8ee-2288">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2288">Type</span></span>  | <span data-ttu-id="9e8ee-2289">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="9e8ee-2290">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2290">Count</span></span> | <span data-ttu-id="9e8ee-2291">13</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="9e8ee-2292">PropertyTagExifInterop</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="9e8ee-2293">Deslocamento para um bloco de itens de propriedade que contêm informações de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="9e8ee-2294">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2294">Property info</span></span> | <span data-ttu-id="9e8ee-2295">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="9e8ee-2296">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2296">Tag</span></span>   | <span data-ttu-id="9e8ee-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2297">0xA005</span></span>              |
| <span data-ttu-id="9e8ee-2298">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2298">Type</span></span>  | <span data-ttu-id="9e8ee-2299">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="9e8ee-2300">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2300">Count</span></span> | <span data-ttu-id="9e8ee-2301">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="9e8ee-2302">PropertyTagExifFlashEnergy</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="9e8ee-2303">Energia de estroboscópico, no feixe de BCPS (alimentação de segundos), no momento em que a imagem foi capturada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="9e8ee-2304">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2304">Property info</span></span> | <span data-ttu-id="9e8ee-2305">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2306">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2306">Tag</span></span>   | <span data-ttu-id="9e8ee-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2307">0xA20B</span></span>                  |
| <span data-ttu-id="9e8ee-2308">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2308">Type</span></span>  | <span data-ttu-id="9e8ee-2309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2310">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2310">Count</span></span> | <span data-ttu-id="9e8ee-2311">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="9e8ee-2312">PropertyTagExifSpatialFR</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="9e8ee-2313">Tabela de frequência espacial do dispositivo de entrada e câmera e valores de SFR na largura da imagem, na altura da imagem e na direção diagonal, conforme especificado no ISO 12233.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="9e8ee-2314">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2314">Property info</span></span> | <span data-ttu-id="9e8ee-2315">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2316">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2316">Tag</span></span>   | <span data-ttu-id="9e8ee-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2317">0xA20C</span></span>                   |
| <span data-ttu-id="9e8ee-2318">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2318">Type</span></span>  | <span data-ttu-id="9e8ee-2319">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2320">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2320">Count</span></span> | <span data-ttu-id="9e8ee-2321">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="9e8ee-2322">PropertyTagExifFocalXRes</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="9e8ee-2323">Número de pixels na direção da largura da imagem (x) por unidade no plano focal da câmera.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="9e8ee-2324">A unidade é especificada em PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="9e8ee-2325">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2325">Property info</span></span> | <span data-ttu-id="9e8ee-2326">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2327">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2327">Tag</span></span>   | <span data-ttu-id="9e8ee-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2328">0xA20E</span></span>                  |
| <span data-ttu-id="9e8ee-2329">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2329">Type</span></span>  | <span data-ttu-id="9e8ee-2330">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2331">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2331">Count</span></span> | <span data-ttu-id="9e8ee-2332">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="9e8ee-2333">PropertyTagExifFocalYRes</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="9e8ee-2334">Número de pixels na direção da altura da imagem (y) por unidade no plano focal da câmera.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="9e8ee-2335">A unidade é especificada em PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="9e8ee-2336">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2336">Property info</span></span> | <span data-ttu-id="9e8ee-2337">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2338">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2338">Tag</span></span>   | <span data-ttu-id="9e8ee-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2339">0xA20F</span></span>                  |
| <span data-ttu-id="9e8ee-2340">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2340">Type</span></span>  | <span data-ttu-id="9e8ee-2341">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2342">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2342">Count</span></span> | <span data-ttu-id="9e8ee-2343">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="9e8ee-2344">PropertyTagExifFocalResUnit</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="9e8ee-2345">Unidade de medida para PropertyTagExifFocalXRes e PropertyTagExifFocalYRes.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="9e8ee-2346">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2346">Tag</span></span>

<span data-ttu-id="9e8ee-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2347">0xA210</span></span>

<span data-ttu-id="9e8ee-2348">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2348">Type</span></span>

<span data-ttu-id="9e8ee-2349">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2350">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2350">Count</span></span>

<span data-ttu-id="9e8ee-2351">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2351">1</span></span>

<span data-ttu-id="9e8ee-2352">2 polegadas e 3 centímetros</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="9e8ee-2353">PropertyTagExifSubjectLoc</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="9e8ee-2354">Local do assunto principal na cena.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="9e8ee-2355">O valor dessa marca representa o pixel no centro do assunto principal relativo à borda esquerda.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="9e8ee-2356">O primeiro valor indica o número da coluna e o segundo valor indica o número da linha.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="9e8ee-2357">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2357">Property info</span></span> | <span data-ttu-id="9e8ee-2358">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="9e8ee-2359">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2359">Tag</span></span>   | <span data-ttu-id="9e8ee-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2360">0xA214</span></span>               |
| <span data-ttu-id="9e8ee-2361">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2361">Type</span></span>  | <span data-ttu-id="9e8ee-2362">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="9e8ee-2363">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2363">Count</span></span> | <span data-ttu-id="9e8ee-2364">2</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="9e8ee-2365">PropertyTagExifExposureIndex</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="9e8ee-2366">Índice de exposição selecionado na câmera ou no dispositivo de entrada no momento em que a imagem foi capturada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="9e8ee-2367">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2367">Property info</span></span> | <span data-ttu-id="9e8ee-2368">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="9e8ee-2369">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2369">Tag</span></span>   | <span data-ttu-id="9e8ee-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2370">0xA215</span></span>                  |
| <span data-ttu-id="9e8ee-2371">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2371">Type</span></span>  | <span data-ttu-id="9e8ee-2372">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="9e8ee-2373">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2373">Count</span></span> | <span data-ttu-id="9e8ee-2374">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="9e8ee-2375">PropertyTagExifSensingMethod</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="9e8ee-2376">Tipo de sensor de imagem na câmera ou no dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="9e8ee-2377">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2377">Tag</span></span>

<span data-ttu-id="9e8ee-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2378">0xA217</span></span>

<span data-ttu-id="9e8ee-2379">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2379">Type</span></span>

<span data-ttu-id="9e8ee-2380">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="9e8ee-2381">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2381">Count</span></span>

<span data-ttu-id="9e8ee-2382">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2382">1</span></span>

<span data-ttu-id="9e8ee-2383">1-não definido 2 – sensor de área de cor de um chip 3-dois-chips sensor de área de cores 4-três chips sensor de área de cores 5-cor sequencial de área do sensor 7-triline sensor linear de cor outro-reservado</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="9e8ee-2384">PropertyTagExifFileSource</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="9e8ee-2385">A origem da imagem.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2385">The image source.</span></span> <span data-ttu-id="9e8ee-2386">Se uma DSC registrou a imagem, o valor dessa marca será 3.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="9e8ee-2387">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2387">Property info</span></span> | <span data-ttu-id="9e8ee-2388">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2389">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2389">Tag</span></span>   | <span data-ttu-id="9e8ee-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2390">0xA300</span></span>                   |
| <span data-ttu-id="9e8ee-2391">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2391">Type</span></span>  | <span data-ttu-id="9e8ee-2392">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2393">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2393">Count</span></span> | <span data-ttu-id="9e8ee-2394">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="9e8ee-2395">PropertyTagExifSceneType</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="9e8ee-2396">O tipo de cena.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2396">The type of scene.</span></span> <span data-ttu-id="9e8ee-2397">Se uma DSC registrou a imagem, o valor dessa marca deverá ser definido como 1, indicando que a imagem foi fotografada diretamente.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="9e8ee-2398">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2398">Property info</span></span> | <span data-ttu-id="9e8ee-2399">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2400">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2400">Tag</span></span>   | <span data-ttu-id="9e8ee-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2401">0xA301</span></span>                   |
| <span data-ttu-id="9e8ee-2402">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2402">Type</span></span>  | <span data-ttu-id="9e8ee-2403">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2404">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2404">Count</span></span> | <span data-ttu-id="9e8ee-2405">1</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="9e8ee-2406">PropertyTagExifCfaPattern</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="9e8ee-2407">O padrão geométrico da matriz de filtro de cor (CFA) do sensor de imagem quando um sensor de área de cor de um chip é usado.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="9e8ee-2408">Ele não se aplica a todos os métodos de detecção.</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="9e8ee-2409">Informações da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2409">Property info</span></span> | <span data-ttu-id="9e8ee-2410">Valor</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="9e8ee-2411">Marca</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2411">Tag</span></span>   | <span data-ttu-id="9e8ee-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2412">0xA302</span></span>                   |
| <span data-ttu-id="9e8ee-2413">Type</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2413">Type</span></span>  | <span data-ttu-id="9e8ee-2414">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="9e8ee-2415">Contagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2415">Count</span></span> | <span data-ttu-id="9e8ee-2416">Qualquer</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="9e8ee-2417">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e8ee-2418">Especificações de formato de arquivo de imagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="9e8ee-2419">Constantes de marca de propriedade de imagem</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="9e8ee-2420">**Constantes de tipo de marca de propriedade de imagem**</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="9e8ee-2421">Marcas de propriedade em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="9e8ee-2422">Marcas de propriedade em ordem numérica</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="9e8ee-2423">Lendo e gravando metadados</span><span class="sxs-lookup"><span data-stu-id="9e8ee-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



