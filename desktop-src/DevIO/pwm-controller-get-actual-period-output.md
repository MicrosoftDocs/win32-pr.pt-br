---
description: Contém o período de sinal de saída efetivo para um controlador de modulação de pulsos (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Estrutura de PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646360"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="415f5-103">\_Controlador PWM \_ obter a estrutura de \_ saída do \_ período real \_</span><span class="sxs-lookup"><span data-stu-id="415f5-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="415f5-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="415f5-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="415f5-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="415f5-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="415f5-106">Contém o período de sinal de saída efetivo para um controlador de modulação de pulsos (PWM).</span><span class="sxs-lookup"><span data-stu-id="415f5-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="415f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="415f5-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="415f5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="415f5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="415f5-109">**ActualPeriod**</span><span class="sxs-lookup"><span data-stu-id="415f5-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="415f5-110">O período de sinal de saída efetivo como seria medido nos canais de saída do controlador.</span><span class="sxs-lookup"><span data-stu-id="415f5-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="415f5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="415f5-111">Requirements</span></span>



| <span data-ttu-id="415f5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="415f5-112">Requirement</span></span> | <span data-ttu-id="415f5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="415f5-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415f5-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="415f5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="415f5-115">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="415f5-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="415f5-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="415f5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="415f5-117">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="415f5-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="415f5-118">Versão mínima do KMDF</span><span class="sxs-lookup"><span data-stu-id="415f5-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="415f5-119">1,19</span><span class="sxs-lookup"><span data-stu-id="415f5-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="415f5-120">Versão mínima do UMDF</span><span class="sxs-lookup"><span data-stu-id="415f5-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="415f5-121">2.19</span><span class="sxs-lookup"><span data-stu-id="415f5-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="415f5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="415f5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="415f5-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="415f5-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415f5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="415f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415f5-125">**\_controlador PWM \_ IOCTL \_ obter \_ \_ período real**</span><span class="sxs-lookup"><span data-stu-id="415f5-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




