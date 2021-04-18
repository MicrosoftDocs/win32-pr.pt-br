---
title: Estrutura de WMDM_PROP_VALUES_RANGE
description: A \_ \_ estrutura de intervalo de valores prop do WMDM \_ descreve um intervalo de valores válidos para uma determinada propriedade em uma configuração de propriedade específica.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Estrutura de WMDM_PROP_VALUES_RANGE Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781071"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="0a897-104">\_Estrutura do \_ intervalo de valores prop do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="0a897-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="0a897-105">A estrutura de **\_ \_ \_ intervalo de valores prop do WMDM** descreve um intervalo de valores válidos para uma determinada propriedade em uma configuração de propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="0a897-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a897-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a897-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="0a897-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0a897-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0a897-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="0a897-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="0a897-109">Valor mínimo no intervalo.</span><span class="sxs-lookup"><span data-stu-id="0a897-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="0a897-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="0a897-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="0a897-111">Valor máximo no intervalo.</span><span class="sxs-lookup"><span data-stu-id="0a897-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="0a897-112">**rangeStep**</span><span class="sxs-lookup"><span data-stu-id="0a897-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="0a897-113">O tamanho da etapa em que os valores válidos são incrementados do valor mínimo para o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="0a897-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="0a897-114">Isso permite especificar valores permitidos distintos em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="0a897-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a897-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a897-115">Remarks</span></span>

<span data-ttu-id="0a897-116">Essa estrutura é usada na estrutura [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) para descrever um intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="0a897-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="0a897-117">Um intervalo de valores válidos é aplicável quando \_ SqlEnum \_ prop \_ \_ valores válidos \_ enum é selecionado na enumeração [**de \_ \_ \_ \_ \_ formato de valores válidos de prop enum**](wmdm-enum-prop-valid-values-form.md)</span><span class="sxs-lookup"><span data-stu-id="0a897-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a897-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a897-118">Requirements</span></span>



| <span data-ttu-id="0a897-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a897-119">Requirement</span></span> | <span data-ttu-id="0a897-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0a897-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0a897-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a897-121">Header</span></span><br/> | <dl> <span data-ttu-id="0a897-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a897-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a897-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a897-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a897-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="0a897-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="0a897-125">**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="0a897-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="0a897-126">**\_funcionalidade de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="0a897-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="0a897-127">**\_configuração de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="0a897-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="0a897-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="0a897-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="0a897-129">**\_enumeração de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="0a897-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="0a897-130">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="0a897-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





