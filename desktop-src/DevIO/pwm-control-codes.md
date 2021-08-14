---
description: Este tópico lista os IOCTLs para modulação de largura de pulso.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Códigos de controle PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9118d51721165860d6132cb7f0fc91a0ac95e7a9d92446df27076a625c83b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405200"
---
# <a name="pwm-control-codes"></a>Códigos de controle PWM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Este tópico lista os IOCTLs para modulação de largura de pulso.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_controlador PWM \_ IOCTL \_ obter \_ \_ período real**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Recupera o período de sinal de saída efetivo do controlador de modulação de largura de pulso (PWM), pois ele seria medido em seus canais de saída.<br/>                                                                                                                                                                                  |
| [**\_ \_ \_ obter informações do controlador PWM do IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Recupera informações sobre um controlador de modulação de largura de pulso (PWM). Essas informações não são alteradas depois que o controlador é inicializado. <br/>                                                                                                                                                                                |
| [**\_ \_ \_ período desejado do conjunto de controladores \_ PWM do \_ IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Define o período de sinal de saída de um controlador de modulação de largura de pulso (PWM) para um valor sugerido. <br/>                                                                                                                                                                                                                            |
| [**IOCTL \_ PWM \_ PIN \_ obter \_ \_ percentual de \_ ciclo de imposto ativo \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Recupera a porcentagem de ciclo de serviço atual para um PIN ou canal. O código de controle retorna a porcentagem como um [**PIN PWM obter a estrutura de \_ \_ \_ \_ \_ \_ \_ saída percentual do ciclo de imposto ativo**](pwm-pin-get-active-duty-cycle-percentage-output.md) .<br/>                                                                                  |
| [**IOCTL \_ PWM \_ PIN \_ definir \_ o \_ \_ percentual do ciclo de imposto ativo \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Defina um valor de porcentagem de ciclo de serviço desejado para o PIN do controlador ou canal. O código de controle Especifica a porcentagem como uma estrutura de [**\_ entrada de \_ \_ \_ \_ \_ percentual de \_ ciclo de serviço ativo definido pelo PIN PWM**](pwm-pin-set-active-duty-cycle-percentage-input.md) . <br/>                                                                      |
| [**IOCTL \_ PWM \_ PIN \_ obter \_ polaridade**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Recupera a polaridade do sinal atual do PIN ou canal. O código de controle obtém a polaridade de sinal como uma estrutura de [**\_ saída de obtenção de \_ \_ \_ polaridade de PIN PWM**](pwm-pin-get-polarity-output.md) . A polaridade do sinal está ativa alta ou ativa baixa, conforme definido na enumeração de [**\_ polaridade PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . <br/> |
| [**IOCTL \_ PWM \_ PIN \_ set \_ polaridade**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Define a polaridade do sinal do PIN ou canal. O código de controle define a polaridade de sinal com base em uma estrutura de [**entrada de polaridade de \_ conjunto de PIN \_ \_ \_ PWM**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) . A polaridade do sinal está ativa alta ou ativa baixa, conforme definido na enumeração de [**\_ polaridade PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .<br/>           |
| [**\_início do \_ PIN do PWM do IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Inicia a geração do sinal de PWM (modulação de largura de pulso) em um PIN ou canal. Para verificar se um PIN foi iniciado, use [**o \_ PIN PWM do IOCTL \_ \_ \_ iniciado**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**\_parada de \_ PIN \_ PWM de IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Interrompe a geração do sinal de modulação de largura de pulso (PWM) em um PIN ou canal. Para verificar se um PIN foi iniciado, use [**o \_ PIN PWM do IOCTL \_ \_ \_ iniciado**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**o \_ PIN PWM do IOCTL \_ \_ foi \_ iniciado**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Recupera o estado da geração de sinal para um PIN ou canal. Cada PIN tem um estado de iniciado ou parado, pois [**um \_ PIN PWM \_ é \_ iniciado \_**](pwm-pin-is-started-output.md) na estrutura de saída.<br/>                                                                                                                                 |



 

 

 




