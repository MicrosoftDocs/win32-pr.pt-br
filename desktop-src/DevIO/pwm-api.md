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
ms.openlocfilehash: 2ff257007180cf3da2b78c14415c8fa350b4bb395e0202f49d2d7ae056f025bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405190"
---
# <a name="pwm-api"></a>API PWM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A modulação de largura de pulso (PWM) é a técnica de gerar uma onda de pulso retangular que tem uma largura de pulso que é modulada para resultar na variação do valor médio da forma de onda. Os usos mais comuns incluem a condução de motores de servo, LEDs de esmaecimento ou outras funções relacionadas. O PWM destina-se a ser usado principalmente para cenários de Internet das Coisas.

## <a name="about-pulse-width-modulation"></a>Sobre a modulação de largura de pulso

Uma PWM de onda pode ser categorizada por dois parâmetros:

-   Um período de onda (T)

-   O ciclo de serviço, em que a frequência de formato de onda (f) é o recíproco do período de f = 1/T

O ciclo de serviço descreve a proporção do  / tempo **ativo** em relação ao intervalo regular ou ao **período** de tempo. Um ciclo de serviço baixo corresponde a uma média de pouca energia de saída, pois a energia está desligada pela maioria das vezes. O ciclo de imposto é expresso como uma porcentagem. Totalmente em é 100%. Totalmente desativado é 0%. A metade da hora **ativa** é de 50%.

Os desenvolvedores que procuram implementar PWM em seus aplicativos de IoT devem investigar a [documentação do PWM do WinRT.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipos de modulação de largura de pulso

O PWM usa [esses códigos de controle de es](pwm-control-codes.md), [estruturas](pwm-structures.md)e [enumerações.](pwm-enumeration-types.md)

O PWM também usa a seguinte função: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
