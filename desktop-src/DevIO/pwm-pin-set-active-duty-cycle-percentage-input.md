---
description: Contém uma porcentagem de ciclo de serviço desejado para um PIN ou canal em um controlador de modulação de largura de pulso (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Estrutura de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370358"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="487ff-103">\_Estrutura de \_ \_ entrada de \_ \_ percentual de ciclo de serviço ativo da \_ definição \_ de PIN PWM</span><span class="sxs-lookup"><span data-stu-id="487ff-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="487ff-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="487ff-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="487ff-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="487ff-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="487ff-106">Contém uma porcentagem de ciclo de serviço desejado para um PIN ou canal em um controlador de modulação de largura de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="487ff-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="487ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="487ff-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="487ff-108">Membros</span><span class="sxs-lookup"><span data-stu-id="487ff-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="487ff-109">**Percentual**</span><span class="sxs-lookup"><span data-stu-id="487ff-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="487ff-110">O ciclo de serviço de sinal de PWM desejado, como um percentual de PWM \_ , que é um valor de ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="487ff-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="487ff-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="487ff-111">Requirements</span></span>



| <span data-ttu-id="487ff-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="487ff-112">Requirement</span></span> | <span data-ttu-id="487ff-113">Valor</span><span class="sxs-lookup"><span data-stu-id="487ff-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487ff-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="487ff-114">Minimum supported client</span></span><br/> | <span data-ttu-id="487ff-115">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="487ff-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="487ff-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="487ff-116">Minimum supported server</span></span><br/> | <span data-ttu-id="487ff-117">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="487ff-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="487ff-118">Versão mínima do KMDF</span><span class="sxs-lookup"><span data-stu-id="487ff-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="487ff-119">1,19</span><span class="sxs-lookup"><span data-stu-id="487ff-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="487ff-120">Versão mínima do UMDF</span><span class="sxs-lookup"><span data-stu-id="487ff-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="487ff-121">2.19</span><span class="sxs-lookup"><span data-stu-id="487ff-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="487ff-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="487ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="487ff-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="487ff-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="487ff-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="487ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="487ff-125">**IOCTL \_ PWM \_ PIN \_ definir \_ o \_ \_ percentual do ciclo de imposto ativo \_**</span><span class="sxs-lookup"><span data-stu-id="487ff-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




