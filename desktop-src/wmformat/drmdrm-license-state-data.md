---
title: Estrutura de DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: A estrutura de dados de estado de licença do DRM \_ \_ \_ contém informações sobre as restrições de licença para um direito de DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Formato de mídia do Windows de estrutura de DRM_LICENSE_STATE_DATA
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814009"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="542d0-105">Estrutura de DRM_LICENSE_STATE_DATA (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="542d0-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="542d0-106">A estrutura de dados de estado de licença do DRM contém informações sobre as restrições de licença para um direito de DRM. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="542d0-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="542d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="542d0-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="542d0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="542d0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="542d0-109">**dwStreamId**</span><span class="sxs-lookup"><span data-stu-id="542d0-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-110">Número de fluxo ao qual a licença se aplica.</span><span class="sxs-lookup"><span data-stu-id="542d0-110">Stream number to which the license applies.</span></span> <span data-ttu-id="542d0-111">Deve ser 0, o que indica que a licença se aplica a todos os fluxos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="542d0-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-112">**dwCategory**</span><span class="sxs-lookup"><span data-stu-id="542d0-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-113">Categoria da cadeia de caracteres a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="542d0-113">Category of string to be displayed.</span></span> <span data-ttu-id="542d0-114">Consulte [**\_ categoria de \_ estado \_ de licença do DRM**](drmdrm-license-state-category.md) para obter os valores possíveis e seu significado.</span><span class="sxs-lookup"><span data-stu-id="542d0-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-115">**dwNumCounts**</span><span class="sxs-lookup"><span data-stu-id="542d0-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-116">Número de itens fornecidos em **dwCount**.</span><span class="sxs-lookup"><span data-stu-id="542d0-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="542d0-117">Esse valor geralmente é 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="542d0-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="542d0-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-119">Uma matriz de 0 ou 1 ou mais valores **DWORD** que representam o número de vezes que a ação especificada em **dwCategory** pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="542d0-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="542d0-120">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="542d0-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-121">**dwNumDates**</span><span class="sxs-lookup"><span data-stu-id="542d0-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-122">Número de itens fornecidos em **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="542d0-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="542d0-123">Normalmente, no máximo duas datas são usadas, por exemplo, com uma licença que é válida de uma data até outra data.</span><span class="sxs-lookup"><span data-stu-id="542d0-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-124">**data e hora \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="542d0-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-125">Uma matriz de uma ou mais estruturas **FILETIME** que representam uma ou mais datas na licença.</span><span class="sxs-lookup"><span data-stu-id="542d0-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="542d0-126">O significado de uma determinada data depende do valor de **dwCategory**.</span><span class="sxs-lookup"><span data-stu-id="542d0-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="542d0-127">**dwVague**</span><span class="sxs-lookup"><span data-stu-id="542d0-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="542d0-128">Zero ou mais dos seguintes sinalizadores combinados com um **OR bit a** bit:</span><span class="sxs-lookup"><span data-stu-id="542d0-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="542d0-129">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="542d0-129">Flag</span></span>                                    | <span data-ttu-id="542d0-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="542d0-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542d0-131">dados de estado de licença do DRM \_ \_ \_ \_ vagados</span><span class="sxs-lookup"><span data-stu-id="542d0-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="542d0-132">Se definido, pode haver mais licenças que se aplicam ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="542d0-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="542d0-133">A única maneira de ter certeza sobre as licenças individuais que se aplicam a uma determinada ID de chave é enumerar as licenças.</span><span class="sxs-lookup"><span data-stu-id="542d0-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="542d0-134">Para fazer isso, chame [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando a ID da chave como o parâmetro bstrKID.</span><span class="sxs-lookup"><span data-stu-id="542d0-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="542d0-135">Em seguida, use a interface IWMDRMLicense recuperada para examinar as licenças.</span><span class="sxs-lookup"><span data-stu-id="542d0-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="542d0-136">\_dados de estado da licença DRM \_ \_ \_ OPL \_ presentes</span><span class="sxs-lookup"><span data-stu-id="542d0-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="542d0-137">Se definido, a licença inclui OPLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="542d0-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="542d0-138">dados de estado da licença do DRM \_ \_ \_ \_ SAP \_ presente</span><span class="sxs-lookup"><span data-stu-id="542d0-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="542d0-139">Se definido, o conteúdo deve ser entregue usando o caminho de áudio seguro (SAP).</span><span class="sxs-lookup"><span data-stu-id="542d0-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="542d0-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="542d0-140">Remarks</span></span>

<span data-ttu-id="542d0-141">Essa estrutura é recuperada chamando **IWMDRMLicenseQuery:: QueryLicenseState**.</span><span class="sxs-lookup"><span data-stu-id="542d0-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="542d0-142">Se **dwCategory** for **a \_ \_ \_ \_ contagem de estado de licença do WM DRM \_ de \_ until**, a matriz **DateTime** normalmente conterá duas datas: uma data "de" e uma data "until".</span><span class="sxs-lookup"><span data-stu-id="542d0-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="542d0-143">Dois pares de datas também podem ser especificados para criar licenças mais complexas.</span><span class="sxs-lookup"><span data-stu-id="542d0-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="542d0-144">Os elementos da matriz **dwCount** correspondem às datas ou aos intervalos de datas especificados na matriz **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="542d0-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="542d0-145">Se **dwCategory** for **a \_ \_ contagem de \_ estado de licença do WM DRM \_ \_ de \_ until** e **DateTime** contiver um par de datas, então **dwCount** conterá um elemento.</span><span class="sxs-lookup"><span data-stu-id="542d0-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="542d0-146">Se **DateTime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.</span><span class="sxs-lookup"><span data-stu-id="542d0-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="542d0-147">Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="542d0-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="542d0-148">Por exemplo, eles podem ter adquirido uma licença que permitia cinco reproduções até o fim do mês e posteriormente adquiriu uma segunda licença para direitos ilimitados.</span><span class="sxs-lookup"><span data-stu-id="542d0-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="542d0-149">Nesse caso, o \_ sinalizador vago de dados de estado da licença DRM \_ \_ \_ é definido em **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e o componente DRM usará um algoritmo para determinar o conjunto de direitos mais provável que foram aplicados.</span><span class="sxs-lookup"><span data-stu-id="542d0-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="542d0-150">Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.</span><span class="sxs-lookup"><span data-stu-id="542d0-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="542d0-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="542d0-151">Requirements</span></span>



| <span data-ttu-id="542d0-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="542d0-152">Requirement</span></span> | <span data-ttu-id="542d0-153">Valor</span><span class="sxs-lookup"><span data-stu-id="542d0-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="542d0-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="542d0-154">Header</span></span><br/> | <dl> <span data-ttu-id="542d0-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="542d0-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="542d0-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="542d0-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="542d0-157">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="542d0-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





