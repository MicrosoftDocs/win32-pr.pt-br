---
title: Enumeração de WMDM_ENUM_PROP_VALID_VALUES_FORM
description: O \_ tipo de enumeração de formulário valores válidos de prop Enumerate do WMDM \_ \_ \_ \_ descreve possíveis formas de valores válidos para uma propriedade.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM de enumeração do Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781470"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="9a629-104">\_Enumeração de \_ \_ formato de \_ valores válidos de prop enum \_ do WMDM</span><span class="sxs-lookup"><span data-stu-id="9a629-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="9a629-105">O tipo de enumeração de **\_ \_ \_ \_ \_ formulário valores válidos de prop Enumerate do WMDM** descreve possíveis formas de valores válidos para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a629-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a629-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a629-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="9a629-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="9a629-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9a629-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**\_ \_ \_ \_ todos os valores válidos de prop do WMDM enum \_**</span><span class="sxs-lookup"><span data-stu-id="9a629-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="9a629-109">Todos os valores são válidos.</span><span class="sxs-lookup"><span data-stu-id="9a629-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="9a629-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_intervalo de \_ \_ valores válidos \_ de \_ prop do WMDM enum**</span><span class="sxs-lookup"><span data-stu-id="9a629-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="9a629-111">Os valores válidos são expressos como um intervalo.</span><span class="sxs-lookup"><span data-stu-id="9a629-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="9a629-112">Para obter informações detalhadas, consulte a estrutura do [**\_ intervalo de \_ valores \_ de prop**](wmdm-prop-values-range.md) . do WMDM.</span><span class="sxs-lookup"><span data-stu-id="9a629-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a629-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_enumeração de \_ \_ valores válidos \_ de \_ prop do WMDM enum**</span><span class="sxs-lookup"><span data-stu-id="9a629-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="9a629-114">Os valores válidos são um conjunto enumerado.</span><span class="sxs-lookup"><span data-stu-id="9a629-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="9a629-115">Para obter informações detalhadas, consulte a estrutura de [**\_ enumeração de \_ valores \_ de prop**](wmdm-prop-values-enum.md) . do WMDM.</span><span class="sxs-lookup"><span data-stu-id="9a629-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a629-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a629-116">Remarks</span></span>

<span data-ttu-id="9a629-117">Essa enumeração é usada na estrutura [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) para especificar a forma de valores válidos para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="9a629-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a629-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a629-118">Requirements</span></span>



| <span data-ttu-id="9a629-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a629-119">Requirement</span></span> | <span data-ttu-id="9a629-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a629-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a629-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a629-121">Header</span></span><br/> | <dl> <span data-ttu-id="9a629-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a629-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a629-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a629-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a629-124">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="9a629-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="9a629-125">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="9a629-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="9a629-126">**\_funcionalidade de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9a629-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="9a629-127">**\_configuração de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9a629-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="9a629-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9a629-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="9a629-129">**\_enumeração de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9a629-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="9a629-130">**\_intervalo de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9a629-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





