---
title: Estrutura de WMDM_PROP_VALUES_ENUM
description: A \_ estrutura de enumeração de valores prop do WMDM \_ \_ contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Estrutura de WMDM_PROP_VALUES_ENUM Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813203"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="e6a8b-104">\_Estrutura de \_ enumeração de valores de prop WMDM \_</span><span class="sxs-lookup"><span data-stu-id="e6a8b-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="e6a8b-105">A estrutura de **\_ \_ \_ enumeração de valores prop do WMDM** contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a8b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6a8b-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="e6a8b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e6a8b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6a8b-108">**cEnumValues**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="e6a8b-109">Contagem de valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="e6a8b-110">**Valores principais**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="e6a8b-111">Ponteiro para uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-111">Pointer to an array of values.</span></span> <span data-ttu-id="e6a8b-112">O tamanho da matriz é igual ao valor de **cEnumValues**.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6a8b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6a8b-113">Remarks</span></span>

<span data-ttu-id="e6a8b-114">Essa estrutura é usada na estrutura **\_ \_ desc prop do WMDM** para descrever um conjunto enumerado de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="e6a8b-115">Um conjunto enumerado de valores válidos é aplicável quando \_ SqlEnum \_ prop \_ \_ valores válidos \_ enum é selecionado na enumeração **de \_ \_ \_ \_ \_ formato de valores válidos de prop enum do WMDM** .</span><span class="sxs-lookup"><span data-stu-id="e6a8b-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="e6a8b-116">O chamador é necessário para liberar a memória usada por **valores principais**.</span><span class="sxs-lookup"><span data-stu-id="e6a8b-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="e6a8b-117">Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="e6a8b-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a8b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6a8b-118">Requirements</span></span>



| <span data-ttu-id="e6a8b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a8b-119">Requirement</span></span> | <span data-ttu-id="e6a8b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e6a8b-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a8b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6a8b-121">Header</span></span><br/> | <dl> <span data-ttu-id="e6a8b-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6a8b-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a8b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6a8b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a8b-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="e6a8b-125">**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="e6a8b-126">**\_funcionalidade de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="e6a8b-127">**\_configuração de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="e6a8b-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="e6a8b-129">**\_intervalo de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="e6a8b-130">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="e6a8b-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





