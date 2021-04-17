---
title: Estrutura de WMDM_PROP_DESC
description: A estrutura do WMDM \_ prop \_ desc descreve os valores válidos de uma propriedade em uma configuração de propriedade específica.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Estrutura de WMDM_PROP_DESC Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759757"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="d7968-104">\_Estrutura desc prop do WMDM \_</span><span class="sxs-lookup"><span data-stu-id="d7968-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="d7968-105">A estrutura do **WMDM \_ prop \_ desc** descreve os valores válidos de uma propriedade em uma configuração de propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="d7968-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7968-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7968-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="d7968-107">Membros</span><span class="sxs-lookup"><span data-stu-id="d7968-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7968-108">**pwszPropName**</span><span class="sxs-lookup"><span data-stu-id="d7968-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="d7968-109">Nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="d7968-109">Name of the property.</span></span> <span data-ttu-id="d7968-110">O aplicativo deve liberar essa memória quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="d7968-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="d7968-111">**ValidValuesForm**</span><span class="sxs-lookup"><span data-stu-id="d7968-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="d7968-112">Um valor de enumeração do [**\_ \_ \_ \_ \_ formulário de valores válidos da prop do WMDM enum**](wmdm-enum-prop-valid-values-form.md) que descreve o tipo de valores, como um intervalo ou uma lista.</span><span class="sxs-lookup"><span data-stu-id="d7968-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="d7968-113">O valor dessa enumeração determina qual variável de membro é usada.</span><span class="sxs-lookup"><span data-stu-id="d7968-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="d7968-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="d7968-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="d7968-115">Mantém os valores válidos da propriedade em uma configuração de propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="d7968-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="d7968-116">Esse membro contém um dos três itens: o valor de enumeração \_ WMDM \_ enum \_ prop \_ Values válidos \_ any; o membro **ValidValuesRange**; ou o membro **EnumeratedValidValues**.</span><span class="sxs-lookup"><span data-stu-id="d7968-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="d7968-117">O valor ou o membro é indicado por **ValidValuesForm**.</span><span class="sxs-lookup"><span data-stu-id="d7968-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="d7968-118">**ValidValuesRange**</span><span class="sxs-lookup"><span data-stu-id="d7968-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="d7968-119">Uma estrutura de [**\_ \_ \_ intervalo de valores prop do WMDM**](wmdm-prop-values-range.md) que contém um intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="d7968-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="d7968-120">Isso está presente somente quando **ValidValuesForm** está definido como WMDM \_ enum \_ prop \_ \_ valores válidos \_ Range.</span><span class="sxs-lookup"><span data-stu-id="d7968-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="d7968-121">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d7968-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d7968-122">**EnumeratedValidValues**</span><span class="sxs-lookup"><span data-stu-id="d7968-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="d7968-123">Uma estrutura de [**\_ \_ \_ enumeração de valores prop do WMDM**](wmdm-prop-values-enum.md) que contém um conjunto enumerado de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="d7968-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="d7968-124">Isso só estará presente quando **ValidValuesForm** for definido como WMDM \_ enum \_ prop \_ \_ valores válidos \_ enum.</span><span class="sxs-lookup"><span data-stu-id="d7968-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="d7968-125">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d7968-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7968-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7968-126">Remarks</span></span>

<span data-ttu-id="d7968-127">A **estrutura \_ \_ desc prop do WMDM** contém uma descrição de propriedade que consiste em um nome de propriedade e seus valores válidos em uma configuração específica.</span><span class="sxs-lookup"><span data-stu-id="d7968-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="d7968-128">O chamador é necessário para liberar a memória usada por **ValidValuesRange** ou **EnumeratedValues**.</span><span class="sxs-lookup"><span data-stu-id="d7968-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="d7968-129">Para obter um exemplo de como fazer isso, consulte [**a \_ \_ funcionalidade de formato WMDM**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="d7968-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7968-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7968-130">Requirements</span></span>



| <span data-ttu-id="d7968-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7968-131">Requirement</span></span> | <span data-ttu-id="d7968-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d7968-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7968-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7968-133">Header</span></span><br/> | <dl> <span data-ttu-id="d7968-134"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7968-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7968-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7968-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7968-136">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="d7968-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="d7968-137">**\_formulário de \_ \_ valores válidos \_ de prop Enumeração WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d7968-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="d7968-138">**\_funcionalidade de formato WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d7968-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="d7968-139">**\_configuração de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d7968-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="d7968-140">**\_enumeração de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d7968-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="d7968-141">**\_intervalo de \_ valores de prop do WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="d7968-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="d7968-142">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="d7968-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





