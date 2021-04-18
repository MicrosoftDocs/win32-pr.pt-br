---
description: O \_ tipo de enumeração de tipos de uso de parâmetro WPD \_ \_ descreve como um parâmetro de método é usado em um determinado método.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumeração de WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751543"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="ed1a7-103">\_Enumeração de \_ tipos de uso de parâmetro WPD \_</span><span class="sxs-lookup"><span data-stu-id="ed1a7-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="ed1a7-104">O tipo de enumeração de [**\_ tipos de \_ uso \_ de parâmetro WPD**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) descreve como um parâmetro de método é usado em um determinado método.</span><span class="sxs-lookup"><span data-stu-id="ed1a7-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed1a7-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="ed1a7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ed1a7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed1a7-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_retorno de \_ uso de parâmetro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="ed1a7-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="ed1a7-108">O parâmetro receberá o valor de retorno, se especificado pelo método.</span><span class="sxs-lookup"><span data-stu-id="ed1a7-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="ed1a7-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ uso de parâmetro WPD \_ em**</span><span class="sxs-lookup"><span data-stu-id="ed1a7-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="ed1a7-110">O parâmetro contém um valor de entrada antes que o método seja chamado.</span><span class="sxs-lookup"><span data-stu-id="ed1a7-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="ed1a7-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_uso de parâmetro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed1a7-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="ed1a7-112">O parâmetro contém um valor de saída quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="ed1a7-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="ed1a7-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_uso de parâmetro de WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed1a7-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="ed1a7-114">O parâmetro contém um valor de entrada antes que o método seja chamado e um valor de saída quando ele retorna.</span><span class="sxs-lookup"><span data-stu-id="ed1a7-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed1a7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1a7-115">Requirements</span></span>



| <span data-ttu-id="ed1a7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1a7-116">Requirement</span></span> | <span data-ttu-id="ed1a7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed1a7-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1a7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed1a7-118">Header</span></span><br/> | <dl> <span data-ttu-id="ed1a7-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1a7-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

