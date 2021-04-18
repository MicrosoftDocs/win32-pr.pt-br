---
description: O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propriedades da proteção contra cópia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810237"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="d03a3-104">Conjunto de propriedades da proteção contra cópia de DVD</span><span class="sxs-lookup"><span data-stu-id="d03a3-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="d03a3-105">O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="d03a3-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="d03a3-106">Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.</span><span class="sxs-lookup"><span data-stu-id="d03a3-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="d03a3-107">A Microsoft fornece software que facilita o processo de autenticação exigido pelo esquema de criptografia, permitindo, assim, uma unidade de DVD-ROM para autenticar e transferir chaves com um DVD Decrypter.</span><span class="sxs-lookup"><span data-stu-id="d03a3-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="d03a3-108">A Microsoft não tem planos atuais para enviar um DVD Decrypter e, em vez disso, está fornecendo código do sistema operacional que atuará como agente para habilitar a autenticação de descriptografadores de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="d03a3-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="d03a3-109">O navegador de DVD inicia e controla o processo de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="d03a3-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="d03a3-110">O DVD minidriver precisa apenas implementar as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="d03a3-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="d03a3-111">Outros componentes manipulam o restante.</span><span class="sxs-lookup"><span data-stu-id="d03a3-111">Other components handle the rest.</span></span>

<span data-ttu-id="d03a3-112">Cada fluxo de entrada de DVD receberá Propriedades de proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="d03a3-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="d03a3-113">Isso é verdadeiro mesmo que o mesmo hardware controle todos os fluxos de DVD.</span><span class="sxs-lookup"><span data-stu-id="d03a3-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="d03a3-114">As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="d03a3-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="d03a3-115">Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="d03a3-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="d03a3-116">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="d03a3-116">Property Set GUID</span></span> | <span data-ttu-id="d03a3-117">\_KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="d03a3-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d03a3-118">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="d03a3-118">Property ID</span></span></th>
<th><span data-ttu-id="d03a3-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d03a3-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d03a3-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d03a3-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="d03a3-121">Consulta se a saída de vídeo é um vídeo de componente analógico e de definição padrão.</span><span class="sxs-lookup"><span data-stu-id="d03a3-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03a3-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="d03a3-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="d03a3-123">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="d03a3-123">This is a set-only property.</span></span> <span data-ttu-id="d03a3-124">Essa propriedade define o nível de proteção de cópia analógica para o codificador NTSC na extremidade de saída do PIN de recebimento.</span><span class="sxs-lookup"><span data-stu-id="d03a3-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="d03a3-125">Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03a3-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="d03a3-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="d03a3-127">As operações Get e Set têm suporte nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d03a3-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="d03a3-128">Uma operação get solicita que o decodificador forneça sua chave de desafio de barramento.</span><span class="sxs-lookup"><span data-stu-id="d03a3-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="d03a3-129">Uma operação de definição fornece o decodificador com a chave de desafio de barramento da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="d03a3-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="d03a3-130">Os dados passados nesta propriedade serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03a3-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="d03a3-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="d03a3-132">Esta é uma propriedade somente obtenção.</span><span class="sxs-lookup"><span data-stu-id="d03a3-132">This is a get-only property.</span></span> <span data-ttu-id="d03a3-133">Essa propriedade solicita que a tecla de barramento 2 do decodificador seja transferida para a unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="d03a3-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="d03a3-134">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03a3-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="d03a3-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="d03a3-136">Propriedade Set-only.</span><span class="sxs-lookup"><span data-stu-id="d03a3-136">Set-only property.</span></span> <span data-ttu-id="d03a3-137">Isso fornece a chave do disco.</span><span class="sxs-lookup"><span data-stu-id="d03a3-137">This provides disc key.</span></span> <span data-ttu-id="d03a3-138">A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03a3-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="d03a3-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="d03a3-140">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="d03a3-140">This is a set-only property.</span></span> <span data-ttu-id="d03a3-141">Essa propriedade fornece a chave 1 do barramento de unidade de DVD para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="d03a3-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="d03a3-142">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03a3-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="d03a3-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="d03a3-144">Código de região solicita a definição de região que o decodificador tem permissão para reproduzir, conforme definido pelo DVD Consortium.</span><span class="sxs-lookup"><span data-stu-id="d03a3-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="d03a3-145">Essa região é definida como uma estrutura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d03a3-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03a3-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="d03a3-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="d03a3-147">Tanto Get quanto Set têm suporte nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d03a3-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="d03a3-148">Get é chamado primeiro para determinar se a autenticação é necessária.</span><span class="sxs-lookup"><span data-stu-id="d03a3-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="d03a3-149">As propriedades definidas são indicações sobre qual fase da negociação de proteção de cópia o filtro está inserindo.</span><span class="sxs-lookup"><span data-stu-id="d03a3-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="d03a3-150">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d03a3-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="d03a3-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="d03a3-152">Se essa propriedade for <strong>true</strong>, o navegador de DVD não enviará amostras de <strong>AM_UseNewCSSKey</strong> antes de negociar a chave de disco.</span><span class="sxs-lookup"><span data-stu-id="d03a3-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="d03a3-153">Consulte <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="d03a3-154">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d03a3-154">Read-only.</span></span> <span data-ttu-id="d03a3-155">Os dados da propriedade são um valor <strong>bool</strong> .</span><span class="sxs-lookup"><span data-stu-id="d03a3-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d03a3-156">Aplica-se ao Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d03a3-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d03a3-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="d03a3-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="d03a3-158">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="d03a3-158">This is a set-only property.</span></span> <span data-ttu-id="d03a3-159">Isso fornece a chave de título do conteúdo atual.</span><span class="sxs-lookup"><span data-stu-id="d03a3-159">This provides title key from current content.</span></span> <span data-ttu-id="d03a3-160">A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d03a3-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d03a3-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d03a3-161">Requirements</span></span>



| <span data-ttu-id="d03a3-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d03a3-162">Requirement</span></span> | <span data-ttu-id="d03a3-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d03a3-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d03a3-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d03a3-164">Header</span></span><br/> | <dl> <span data-ttu-id="d03a3-165"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="d03a3-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03a3-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="d03a3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03a3-167">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="d03a3-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




