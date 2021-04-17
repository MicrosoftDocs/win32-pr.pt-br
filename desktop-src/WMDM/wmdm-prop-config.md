---
title: Estrutura de WMDM_PROP_CONFIG
description: A \_ estrutura de configuração do sqlprop \_ descreve um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte pelo dispositivo para um determinado formato. Essa estrutura contém várias descrições de propriedade em uma matriz de \_ estruturas desc prop do WMDM \_ .
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Estrutura de WMDM_PROP_CONFIG Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813396"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="8b499-105">Estrutura de configuração de \_ prop do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="8b499-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="8b499-106">A estrutura de **\_ \_ configuração do sqlprop** descreve um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte pelo dispositivo para um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="8b499-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="8b499-107">Essa estrutura contém várias descrições de propriedade em uma matriz de estruturas [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="8b499-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b499-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b499-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="8b499-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8b499-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b499-110">**nPreference**</span><span class="sxs-lookup"><span data-stu-id="8b499-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="8b499-111">Nível de preferência do dispositivo para esta configuração.</span><span class="sxs-lookup"><span data-stu-id="8b499-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="8b499-112">O valor mais baixo indica a configuração mais preferencial.</span><span class="sxs-lookup"><span data-stu-id="8b499-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8b499-113">**nPropDesc**</span><span class="sxs-lookup"><span data-stu-id="8b499-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="8b499-114">Número de descrições de propriedade contidas nessa configuração.</span><span class="sxs-lookup"><span data-stu-id="8b499-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="8b499-115">Há uma única descrição de propriedade para cada propriedade com suporte para o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="8b499-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="8b499-116">**pPropDesc**</span><span class="sxs-lookup"><span data-stu-id="8b499-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="8b499-117">Ponteiro para uma matriz de [**estruturas \_ \_ desc prop do WMDM**](wmdm-prop-desc.md) contendo descrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8b499-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="8b499-118">O tamanho da matriz é igual ao valor de **nPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="8b499-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="8b499-119">O aplicativo deve liberar essa memória quando terminar com ela.</span><span class="sxs-lookup"><span data-stu-id="8b499-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b499-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b499-120">Remarks</span></span>

<span data-ttu-id="8b499-121">A estrutura de [**\_ \_ recursos de formato WMDM**](wmdm-format-capability.md) retornada por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) para um formato específico consiste em um número de configurações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8b499-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="8b499-122">**WMDM \_ As \_** estruturas de configuração da prop descrevem essas configurações.</span><span class="sxs-lookup"><span data-stu-id="8b499-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="8b499-123">Uma configuração de propriedade descreve valores para todas as propriedades com suporte para um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="8b499-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="8b499-124">Os valores de propriedades diferentes em uma única configuração são compatíveis entre si.</span><span class="sxs-lookup"><span data-stu-id="8b499-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="8b499-125">Por exemplo, para um arquivo de áudio, uma configuração incluirá valores válidos de taxa de amostra e valores válidos da taxa de bits, de modo que todas as combinações dessas taxas de amostra e de bits possam ser reproduzidas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b499-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="8b499-126">O chamador é necessário para liberar a memória usada pelo **pPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="8b499-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="8b499-127">Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="8b499-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b499-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b499-128">Requirements</span></span>



| <span data-ttu-id="8b499-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b499-129">Requirement</span></span> | <span data-ttu-id="8b499-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8b499-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8b499-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b499-131">Header</span></span><br/> | <dl> <span data-ttu-id="8b499-132"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b499-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b499-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b499-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b499-134">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="8b499-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="8b499-135">**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="8b499-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="8b499-136">**\_funcionalidade de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="8b499-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="8b499-137">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="8b499-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="8b499-138">**\_enumeração de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="8b499-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="8b499-139">**\_intervalo de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="8b499-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="8b499-140">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="8b499-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





