---
title: Estrutura de DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: A estrutura de dados de estado de licença do DRM \_ \_ \_ contém informações de licença sobre um direito de DRM especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Formato de mídia do Windows de estrutura de DRM_LICENSE_STATE_DATA
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762937"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="87e3b-105">Estrutura de DRM_LICENSE_STATE_DATA (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="87e3b-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="87e3b-106">A estrutura de **dados de estado de licença do DRM \_ \_ \_** contém informações de [*licença*](wmformat-glossary.md) sobre um direito de [*DRM*](wmformat-glossary.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="87e3b-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e3b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87e3b-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="87e3b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="87e3b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="87e3b-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="87e3b-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-110">Número de fluxo ao qual a licença se aplica.</span><span class="sxs-lookup"><span data-stu-id="87e3b-110">Stream number to which the license applies.</span></span> <span data-ttu-id="87e3b-111">Deve ser 0, o que indica que a licença se aplica a todos os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="87e3b-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="87e3b-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-113">Categoria da cadeia de caracteres a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="87e3b-113">Category of string to be displayed.</span></span> <span data-ttu-id="87e3b-114">Consulte [**\_ categoria de \_ estado \_ de licença do DRM**](drm-license-state-category.md) para obter os valores possíveis e seu significado.</span><span class="sxs-lookup"><span data-stu-id="87e3b-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="87e3b-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-116">Número de itens fornecidos em **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="87e3b-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="87e3b-117">Esse valor geralmente é 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="87e3b-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="87e3b-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-119">Uma matriz de 0 ou 1 ou mais **DWORD** s que representa o número de vezes que a ação especificada em **dwCategory** pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="87e3b-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="87e3b-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="87e3b-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="87e3b-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-122">Número de itens fornecidos em **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="87e3b-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="87e3b-123">Normalmente, no máximo duas datas são usadas, por exemplo, com uma licença que é válida de uma data até outra data.</span><span class="sxs-lookup"><span data-stu-id="87e3b-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-124">**data e hora \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="87e3b-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-125">Uma matriz de uma ou mais estruturas FILETIME que representam uma ou mais datas na licença.</span><span class="sxs-lookup"><span data-stu-id="87e3b-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="87e3b-126">O significado de uma determinada data depende do valor de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="87e3b-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="87e3b-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="87e3b-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="87e3b-128">Zero ou mais dos seguintes sinalizadores combinados com um **OR bit a** bit:</span><span class="sxs-lookup"><span data-stu-id="87e3b-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="87e3b-129">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="87e3b-129">Flag</span></span>                                    | <span data-ttu-id="87e3b-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="87e3b-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e3b-131">dados de estado de licença do DRM \_ \_ \_ \_ vagados</span><span class="sxs-lookup"><span data-stu-id="87e3b-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="87e3b-132">Se definido, pode haver mais licenças que se aplicam ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="87e3b-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="87e3b-133">\_dados de estado da licença DRM \_ \_ \_ OPL \_ presentes</span><span class="sxs-lookup"><span data-stu-id="87e3b-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="87e3b-134">Se definido, a licença inclui OPLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="87e3b-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="87e3b-135">dados de estado da licença do DRM \_ \_ \_ \_ SAP \_ presente</span><span class="sxs-lookup"><span data-stu-id="87e3b-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="87e3b-136">Se definido, o conteúdo deve ser entregue usando o caminho de áudio seguro (SAP).</span><span class="sxs-lookup"><span data-stu-id="87e3b-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87e3b-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="87e3b-137">Remarks</span></span>

<span data-ttu-id="87e3b-138">Essa estrutura é retornada (encapsulada em uma estrutura de dados de estado de licença do WM) de uma chamada para [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando você especifica uma das propriedades de estado de licença DRM. [**\_ \_ \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87e3b-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="87e3b-139">Essas propriedades são:</span><span class="sxs-lookup"><span data-stu-id="87e3b-139">These properties are:</span></span>

-   [<span data-ttu-id="87e3b-140">**\_Reprodução de licensestate DRM \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="87e3b-141">**CopyToCD de licença do DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="87e3b-142">**CopyToSDMIDevice de licença do DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="87e3b-143">**CopyToNonSDMIDevice de licença do DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="87e3b-144">**CollaborativePlay de licença do DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="87e3b-145">**\_Cópia do licensestate do DRM \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="87e3b-146">**PlaylistBurn de licença do DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="87e3b-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="87e3b-147">Se **dwCategory** for **a \_ \_ \_ \_ contagem de estado de licença do WM DRM \_ de \_ until,** a matriz **DateTime** normalmente conterá duas datas, uma data "de" e uma data "until".</span><span class="sxs-lookup"><span data-stu-id="87e3b-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="87e3b-148">Dois pares de datas também podem ser especificados para criar licenças mais complexas.</span><span class="sxs-lookup"><span data-stu-id="87e3b-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="87e3b-149">Os elementos da matriz **dwCount** correspondem às datas ou aos intervalos de datas especificados na matriz **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="87e3b-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="87e3b-150">Se **dwCategory** for **a \_ \_ contagem de \_ estado de licença do WM DRM \_ \_ de \_ until** e **DateTime** contiver um par de datas, então **dwCount** conterá um elemento.</span><span class="sxs-lookup"><span data-stu-id="87e3b-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="87e3b-151">Se **DateTime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.</span><span class="sxs-lookup"><span data-stu-id="87e3b-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="87e3b-152">Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="87e3b-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="87e3b-153">Por exemplo, eles podem ter adquirido uma licença que permitia cinco reproduções até o fim do mês e posteriormente adquiriu uma segunda licença para direitos ilimitados.</span><span class="sxs-lookup"><span data-stu-id="87e3b-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="87e3b-154">Nesse caso, o \_ sinalizador vago de dados de estado da licença DRM \_ \_ \_ é definido em **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e o componente DRM usará um algoritmo para determinar o conjunto de direitos mais provável que foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="87e3b-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="87e3b-155">Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.</span><span class="sxs-lookup"><span data-stu-id="87e3b-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e3b-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e3b-156">Requirements</span></span>



| <span data-ttu-id="87e3b-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e3b-157">Requirement</span></span> | <span data-ttu-id="87e3b-158">Valor</span><span class="sxs-lookup"><span data-stu-id="87e3b-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e3b-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87e3b-159">Minimum supported client</span></span><br/> | <span data-ttu-id="87e3b-160">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87e3b-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="87e3b-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87e3b-161">Minimum supported server</span></span><br/> | <span data-ttu-id="87e3b-162">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87e3b-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="87e3b-163">Versão</span><span class="sxs-lookup"><span data-stu-id="87e3b-163">Version</span></span><br/>                  | <span data-ttu-id="87e3b-164">SDK do Windows Media Format 7 ou versões posteriores do SDK</span><span class="sxs-lookup"><span data-stu-id="87e3b-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="87e3b-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87e3b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="87e3b-166"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e3b-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e3b-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="87e3b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e3b-168">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="87e3b-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

