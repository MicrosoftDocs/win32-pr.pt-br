---
title: Estrutura de WMDM_FORMAT_CAPABILITY
description: A \_ estrutura de \_ recursos de formato WMDM descreve os recursos de um dispositivo para um determinado formato.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- Estrutura de WMDM_FORMAT_CAPABILITY Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796456"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="e40a2-104">Estrutura de recursos de \_ formato WMDM \_</span><span class="sxs-lookup"><span data-stu-id="e40a2-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="e40a2-105">A estrutura de **\_ \_ recursos de formato WMDM** descreve os recursos de um dispositivo para um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="e40a2-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="e40a2-106">Essa estrutura contém um conjunto de configurações de propriedade em uma matriz de estruturas de **\_ \_ configuração de prop do WMDM** .</span><span class="sxs-lookup"><span data-stu-id="e40a2-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="e40a2-107">Cada configuração de propriedade representa um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte para um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="e40a2-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="e40a2-108">O aplicativo pode obter essa estrutura chamando o método **IWMDMDevice3:: GetFormatCapability** e passando o código de formato.</span><span class="sxs-lookup"><span data-stu-id="e40a2-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="e40a2-109">Para obter uma lista de códigos de formato, consulte [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="e40a2-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e40a2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e40a2-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="e40a2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e40a2-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="e40a2-112">**nPropConfig**</span><span class="sxs-lookup"><span data-stu-id="e40a2-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="e40a2-113">Número de configurações de propriedade na matriz **pConfigs** .</span><span class="sxs-lookup"><span data-stu-id="e40a2-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="e40a2-114">**pConfigs**</span><span class="sxs-lookup"><span data-stu-id="e40a2-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="e40a2-115">Ponteiro para uma matriz de estruturas de [**\_ \_ configuração de prop do WMDM**](wmdm-prop-config.md) .</span><span class="sxs-lookup"><span data-stu-id="e40a2-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="e40a2-116">O tamanho da matriz é igual ao valor de **nPropConfig**.</span><span class="sxs-lookup"><span data-stu-id="e40a2-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e40a2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e40a2-117">Remarks</span></span>

<span data-ttu-id="e40a2-118">A estrutura de **\_ \_ recursos de formato WMDM** fornece um mecanismo flexível para expressar os recursos do dispositivo para um determinado formato.</span><span class="sxs-lookup"><span data-stu-id="e40a2-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="e40a2-119">Se o conteúdo for destinado a ser renderizado pelo dispositivo (por exemplo, um arquivo de áudio a ser reproduzido pelo dispositivo), as propriedades do conteúdo deverão corresponder a uma das configurações de propriedade retornadas por [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) na estrutura de **\_ \_ recursos do formato WMDM** .</span><span class="sxs-lookup"><span data-stu-id="e40a2-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="e40a2-120">Por exemplo, para um arquivo de áudio, a taxa de bits e a taxa de amostragem devem satisfazer uma das configurações de propriedade retornadas.</span><span class="sxs-lookup"><span data-stu-id="e40a2-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="e40a2-121">O chamador é responsável por liberar a memória alocada para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="e40a2-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="e40a2-122">A função a seguir demonstra como limpar uma estrutura de **\_ \_ recursos de formato do WMDM** .</span><span class="sxs-lookup"><span data-stu-id="e40a2-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="e40a2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e40a2-123">Requirements</span></span>



| <span data-ttu-id="e40a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40a2-124">Requirement</span></span> | <span data-ttu-id="e40a2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e40a2-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e40a2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e40a2-126">Header</span></span><br/> | <dl> <span data-ttu-id="e40a2-127"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e40a2-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e40a2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e40a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40a2-129">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="e40a2-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="e40a2-130">**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e40a2-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="e40a2-131">**\_configuração de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e40a2-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="e40a2-132">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="e40a2-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="e40a2-133">**\_enumeração de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e40a2-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="e40a2-134">**\_intervalo de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e40a2-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="e40a2-135">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="e40a2-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





