---
description: Contém a porcentagem de ciclo de serviço atual para um PIN ou canal em um controlador de modulação de pulso de pulsação (PWM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Estrutura de PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089195"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="ec3cf-103">PWM \_ PIN \_ obter \_ a \_ \_ estrutura de \_ saída percentual do ciclo de imposto ativo \_</span><span class="sxs-lookup"><span data-stu-id="ec3cf-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="ec3cf-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ec3cf-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="ec3cf-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ec3cf-106">Contém a porcentagem de ciclo de serviço atual para um PIN ou canal em um controlador de modulação de pulso de pulsação (PWM).</span><span class="sxs-lookup"><span data-stu-id="ec3cf-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec3cf-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ec3cf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ec3cf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec3cf-109">**Percentual**</span><span class="sxs-lookup"><span data-stu-id="ec3cf-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="ec3cf-110">O ciclo de serviço de sinal de PWM atual, como um percentual de PWM \_ , que é um valor de ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec3cf-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3cf-111">Requirements</span></span>



| <span data-ttu-id="ec3cf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3cf-112">Requirement</span></span> | <span data-ttu-id="ec3cf-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ec3cf-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3cf-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3cf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3cf-115">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ec3cf-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec3cf-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3cf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3cf-117">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ec3cf-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ec3cf-118">Versão mínima do KMDF</span><span class="sxs-lookup"><span data-stu-id="ec3cf-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="ec3cf-119">1,19</span><span class="sxs-lookup"><span data-stu-id="ec3cf-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="ec3cf-120">Versão mínima do UMDF</span><span class="sxs-lookup"><span data-stu-id="ec3cf-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="ec3cf-121">2.19</span><span class="sxs-lookup"><span data-stu-id="ec3cf-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="ec3cf-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec3cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec3cf-123"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3cf-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3cf-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec3cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3cf-125">**IOCTL \_ PWM \_ PIN \_ obter \_ \_ percentual de \_ ciclo de imposto ativo \_**</span><span class="sxs-lookup"><span data-stu-id="ec3cf-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




