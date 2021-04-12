---
description: A modulação de largura de pulso (PWM) é a técnica de gerar uma onda de pulso retangular que tem uma largura de pulso que é modulada para resultar na variação do valor médio da forma de onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500948"
---
# <a name="pwm-api"></a><span data-ttu-id="c65f5-103">API PWM</span><span class="sxs-lookup"><span data-stu-id="c65f5-103">PWM API</span></span>

<span data-ttu-id="c65f5-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c65f5-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c65f5-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c65f5-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c65f5-106">A modulação de largura de pulso (PWM) é a técnica de gerar uma onda de pulso retangular que tem uma largura de pulso que é modulada para resultar na variação do valor médio da forma de onda.</span><span class="sxs-lookup"><span data-stu-id="c65f5-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="c65f5-107">Os usos mais comuns incluem a condução de motores de servo, LEDs de esmaecimento ou outras funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c65f5-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="c65f5-108">O PWM destina-se a ser usado principalmente para cenários de Internet das Coisas.</span><span class="sxs-lookup"><span data-stu-id="c65f5-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="c65f5-109">Sobre a modulação de largura de pulso</span><span class="sxs-lookup"><span data-stu-id="c65f5-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="c65f5-110">Uma PWM de onda pode ser categorizada por dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="c65f5-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="c65f5-111">Um período de onda (T)</span><span class="sxs-lookup"><span data-stu-id="c65f5-111">A waveform period (T)</span></span>

-   <span data-ttu-id="c65f5-112">O ciclo de serviço, em que a frequência de formato de onda (f) é o recíproco do período de f = 1/T</span><span class="sxs-lookup"><span data-stu-id="c65f5-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="c65f5-113">O ciclo de serviço descreve a proporção do  / tempo **ativo** em relação ao intervalo regular ou ao **período** de tempo.</span><span class="sxs-lookup"><span data-stu-id="c65f5-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="c65f5-114">Um ciclo de serviço baixo corresponde a uma média de pouca energia de saída, pois a energia está desligada pela maioria das vezes.</span><span class="sxs-lookup"><span data-stu-id="c65f5-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="c65f5-115">O ciclo de imposto é expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="c65f5-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="c65f5-116">Totalmente em é 100%.</span><span class="sxs-lookup"><span data-stu-id="c65f5-116">Fully on is 100%.</span></span> <span data-ttu-id="c65f5-117">Totalmente desativado é 0%.</span><span class="sxs-lookup"><span data-stu-id="c65f5-117">Fully off is 0%.</span></span> <span data-ttu-id="c65f5-118">A metade da hora **ativa** é de 50%.</span><span class="sxs-lookup"><span data-stu-id="c65f5-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="c65f5-119">Os desenvolvedores que procuram implementar PWM em seus aplicativos de IoT devem investigar a [documentação do PWM do WinRT.](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="c65f5-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="c65f5-120">Tipos de modulação de largura de pulso</span><span class="sxs-lookup"><span data-stu-id="c65f5-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="c65f5-121">O PWM usa [esses códigos de controle de es](pwm-control-codes.md), [estruturas](pwm-structures.md)e [enumerações.](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="c65f5-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="c65f5-122">O PWM também usa a seguinte função: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="c65f5-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
