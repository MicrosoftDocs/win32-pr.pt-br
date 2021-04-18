---
description: Descreve como um parâmetro (método ou evento) armazena seu valor.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumeração WpdParameterAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749914"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="ee6a5-103">Enumeração WpdParameterAttributeForm</span><span class="sxs-lookup"><span data-stu-id="ee6a5-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="ee6a5-104">O tipo de enumeração [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) descreve como um parâmetro (método ou evento) armazena seu valor.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6a5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee6a5-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="ee6a5-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ee6a5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee6a5-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_formato de atributo de parâmetro WPD \_ \_ \_ não especificado**</span><span class="sxs-lookup"><span data-stu-id="ee6a5-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="ee6a5-108">A forma do parâmetro não foi especificada.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="ee6a5-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_intervalo de \_ formulário de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee6a5-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="ee6a5-110">O parâmetro especifica um intervalo.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="ee6a5-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_enumeração de \_ formulário de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee6a5-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="ee6a5-112">O parâmetro é uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ee6a5-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ expressão regular de formulário de atributo \_ de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ee6a5-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="ee6a5-114">O parâmetro é uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="ee6a5-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_identificador de \_ objeto de atributo de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ee6a5-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="ee6a5-116">O parâmetro é um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="ee6a5-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee6a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee6a5-117">Requirements</span></span>



| <span data-ttu-id="ee6a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee6a5-118">Requirement</span></span> | <span data-ttu-id="ee6a5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ee6a5-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6a5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee6a5-120">Header</span></span><br/> | <dl> <span data-ttu-id="ee6a5-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee6a5-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

