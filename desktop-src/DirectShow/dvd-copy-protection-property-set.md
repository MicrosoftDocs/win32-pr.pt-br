---
description: O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propriedades da proteção contra cópia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909474"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="49c85-104">Conjunto de propriedades da proteção contra cópia de DVD</span><span class="sxs-lookup"><span data-stu-id="49c85-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="49c85-105">O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="49c85-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="49c85-106">Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.</span><span class="sxs-lookup"><span data-stu-id="49c85-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="49c85-107">A Microsoft fornece software que facilita o processo de autenticação exigido pelo esquema de criptografia, permitindo, assim, uma unidade de DVD-ROM para autenticar e transferir chaves com um DVD Decrypter.</span><span class="sxs-lookup"><span data-stu-id="49c85-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="49c85-108">A Microsoft não tem planos atuais para enviar um DVD Decrypter e, em vez disso, está fornecendo código do sistema operacional que atuará como agente para habilitar a autenticação de descriptografadores de hardware ou software.</span><span class="sxs-lookup"><span data-stu-id="49c85-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="49c85-109">O navegador de DVD inicia e controla o processo de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="49c85-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="49c85-110">O DVD minidriver precisa apenas implementar as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="49c85-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="49c85-111">Outros componentes manipulam o restante.</span><span class="sxs-lookup"><span data-stu-id="49c85-111">Other components handle the rest.</span></span>

<span data-ttu-id="49c85-112">Cada fluxo de entrada de DVD receberá Propriedades de proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="49c85-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="49c85-113">Isso é verdadeiro mesmo que o mesmo hardware controle todos os fluxos de DVD.</span><span class="sxs-lookup"><span data-stu-id="49c85-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="49c85-114">As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="49c85-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="49c85-115">Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="49c85-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="49c85-116">Label</span><span class="sxs-lookup"><span data-stu-id="49c85-116">Label</span></span> | <span data-ttu-id="49c85-117">Valor</span><span class="sxs-lookup"><span data-stu-id="49c85-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="49c85-118">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="49c85-118">Property Set GUID</span></span> | <span data-ttu-id="49c85-119">\_KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="49c85-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49c85-120">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="49c85-120">Property ID</span></span></th>
<th><span data-ttu-id="49c85-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="49c85-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49c85-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="49c85-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="49c85-123">Consulta se a saída de vídeo é um vídeo de componente analógico e de definição padrão.</span><span class="sxs-lookup"><span data-stu-id="49c85-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49c85-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="49c85-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="49c85-125">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="49c85-125">This is a set-only property.</span></span> <span data-ttu-id="49c85-126">Essa propriedade define o nível de proteção de cópia analógica para o codificador NTSC na extremidade de saída do PIN de recebimento.</span><span class="sxs-lookup"><span data-stu-id="49c85-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="49c85-127">Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49c85-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="49c85-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="49c85-129">As operações Get e Set têm suporte nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="49c85-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="49c85-130">Uma operação get solicita que o decodificador forneça sua chave de desafio de barramento.</span><span class="sxs-lookup"><span data-stu-id="49c85-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="49c85-131">Uma operação de definição fornece o decodificador com a chave de desafio de barramento da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="49c85-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="49c85-132">Os dados passados nesta propriedade serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49c85-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="49c85-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="49c85-134">Esta é uma propriedade somente obtenção.</span><span class="sxs-lookup"><span data-stu-id="49c85-134">This is a get-only property.</span></span> <span data-ttu-id="49c85-135">Essa propriedade solicita que a tecla de barramento 2 do decodificador seja transferida para a unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="49c85-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="49c85-136">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49c85-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="49c85-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="49c85-138">Propriedade Set-only.</span><span class="sxs-lookup"><span data-stu-id="49c85-138">Set-only property.</span></span> <span data-ttu-id="49c85-139">Isso fornece a chave do disco.</span><span class="sxs-lookup"><span data-stu-id="49c85-139">This provides disc key.</span></span> <span data-ttu-id="49c85-140">A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49c85-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="49c85-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="49c85-142">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="49c85-142">This is a set-only property.</span></span> <span data-ttu-id="49c85-143">Essa propriedade fornece a chave 1 do barramento de unidade de DVD para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="49c85-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="49c85-144">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49c85-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="49c85-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="49c85-146">Código de região solicita a definição de região que o decodificador tem permissão para reproduzir, conforme definido pelo DVD Consortium.</span><span class="sxs-lookup"><span data-stu-id="49c85-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="49c85-147">Essa região é definida como uma estrutura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="49c85-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49c85-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="49c85-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="49c85-149">Tanto Get quanto Set têm suporte nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="49c85-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="49c85-150">Get é chamado primeiro para determinar se a autenticação é necessária.</span><span class="sxs-lookup"><span data-stu-id="49c85-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="49c85-151">As propriedades definidas são indicações sobre qual fase da negociação de proteção de cópia o filtro está inserindo.</span><span class="sxs-lookup"><span data-stu-id="49c85-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="49c85-152">Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49c85-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="49c85-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="49c85-154">Se essa propriedade for <strong>true</strong>, o navegador de DVD não enviará amostras de <strong>AM_UseNewCSSKey</strong> antes de negociar a chave de disco.</span><span class="sxs-lookup"><span data-stu-id="49c85-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="49c85-155">Consulte <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="49c85-156">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="49c85-156">Read-only.</span></span> <span data-ttu-id="49c85-157">Os dados da propriedade são um valor <strong>bool</strong> .</span><span class="sxs-lookup"><span data-stu-id="49c85-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="49c85-158">Aplica-se ao Windows 7.</span><span class="sxs-lookup"><span data-stu-id="49c85-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49c85-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="49c85-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="49c85-160">Esta é uma propriedade somente de conjunto.</span><span class="sxs-lookup"><span data-stu-id="49c85-160">This is a set-only property.</span></span> <span data-ttu-id="49c85-161">Isso fornece a chave de título do conteúdo atual.</span><span class="sxs-lookup"><span data-stu-id="49c85-161">This provides title key from current content.</span></span> <span data-ttu-id="49c85-162">A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49c85-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="49c85-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49c85-163">Requirements</span></span>



| <span data-ttu-id="49c85-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="49c85-164">Requirement</span></span> | <span data-ttu-id="49c85-165">Valor</span><span class="sxs-lookup"><span data-stu-id="49c85-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49c85-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49c85-166">Header</span></span><br/> | <dl> <span data-ttu-id="49c85-167"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c85-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c85-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="49c85-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c85-169">Conjuntos de propriedades</span><span class="sxs-lookup"><span data-stu-id="49c85-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




