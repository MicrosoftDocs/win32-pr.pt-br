---
description: 'Saiba mais sobre: estruturas PWM'
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: Estruturas PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920313"
---
# <a name="pwm-structures"></a><span data-ttu-id="0946e-103">Estruturas PWM</span><span class="sxs-lookup"><span data-stu-id="0946e-103">PWM Structures</span></span>

<span data-ttu-id="0946e-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0946e-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0946e-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0946e-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0946e-106">As seguintes estruturas são usadas com a modulação de largura de pulso:</span><span class="sxs-lookup"><span data-stu-id="0946e-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0946e-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0946e-107">In this section</span></span>



| <span data-ttu-id="0946e-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="0946e-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="0946e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0946e-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0946e-110">**\_controlador PWM \_ obter \_ \_ saída do período real \_**</span><span class="sxs-lookup"><span data-stu-id="0946e-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="0946e-111">Contém o período de sinal de saída efetivo para um controlador de modulação de pulsos (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="0946e-112">**\_informações do controlador PWM \_**</span><span class="sxs-lookup"><span data-stu-id="0946e-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="0946e-113">Representa as informações estáticas que caracterizam um controlador de modulação de pulsos (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="0946e-114">**\_entrada de \_ \_ período desejado \_ \_ do PWM Controller Set**</span><span class="sxs-lookup"><span data-stu-id="0946e-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="0946e-115">Contém um valor de entrada para um período de sinal sugerido para o controlador de modulação de largura de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="0946e-116">**\_saída do \_ \_ período desejado \_ \_ do PWM Controller Set**</span><span class="sxs-lookup"><span data-stu-id="0946e-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="0946e-117">Contém o período de sinal de saída efetivo do controlador de modulação de largura de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="0946e-118">**\_saída do \_ \_ percentual de \_ \_ ciclo de \_ imposto \_ de obtenção de PIN do PWM**</span><span class="sxs-lookup"><span data-stu-id="0946e-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="0946e-119">Contém a porcentagem de ciclo de serviço atual para um PIN ou canal em um controlador de modulação de pulso de pulsação (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="0946e-120">**\_entrada de \_ \_ porcentagem de \_ ciclo de imposto ativo \_ da \_ definição \_ de PIN PWM**</span><span class="sxs-lookup"><span data-stu-id="0946e-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="0946e-121">Contém uma porcentagem de ciclo de serviço desejado para um PIN ou canal em um controlador de modulação de largura de pulso (PWM).</span><span class="sxs-lookup"><span data-stu-id="0946e-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="0946e-122">**\_saída de \_ obtenção de \_ polaridade \_ do PIN PWM**</span><span class="sxs-lookup"><span data-stu-id="0946e-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="0946e-123">Contém um valor de polaridade a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="0946e-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="0946e-124">**\_entrada de \_ polaridade de conjunto de PIN PWM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0946e-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="0946e-125">Contém um valor desejado para a polaridade de um PIN ou canal.</span><span class="sxs-lookup"><span data-stu-id="0946e-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="0946e-126">**saída de PWM \_ PIN \_ \_ iniciada \_**</span><span class="sxs-lookup"><span data-stu-id="0946e-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="0946e-127">Contém o estado atual de geração de sinal de um PIN.</span><span class="sxs-lookup"><span data-stu-id="0946e-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




