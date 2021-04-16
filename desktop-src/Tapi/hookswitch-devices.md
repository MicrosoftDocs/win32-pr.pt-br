---
description: Um dispositivo de telefone pode ter vários dispositivos Hookswitch.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivos Hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ad6f839ec9078831ffe0b04849be2a4393c9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502172"
---
# <a name="hookswitch-devices"></a>Dispositivos Hookswitch

Um dispositivo de telefone pode ter vários dispositivos Hookswitch. Um Hookswitch é a opção que conecta ou desconecta um dispositivo da linha telefônica. Em um telefone, por exemplo, essa é a opção que é ativada automaticamente quando um usuário levanta o receptor da base para obter um novo tom de discagem. A TAPI define três tipos de dispositivos Hookswitch para um telefone: monofone, viva-voz e headset. Cada dispositivo Hookswitch tem um palestrante e um componente de microfone e opera em um dos quatro modos Hookswitch:

-   **Onhook** O dispositivo Hookswitch está conectado e o microfone e o alto-falante estão desabilitados.
-   **Somente microfone** O dispositivo Hookswitch é offhook, seu microfone está habilitado e seu alto-falante está mudo.
-   **Somente palestrante** O dispositivo Hookswitch é offhook, seu microfone está sem áudio e seu alto-falante está habilitado.
-   **Microfone e palestrante** O dispositivo Hookswitch é offhook e o microfone e o alto-falante estão habilitados.

A função [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) é usada para definir o modo de Hookswitch de um ou mais dos dispositivos Hookswitch de um dispositivo de telefone aberto. Por exemplo, para ativar mudo ou desativar o componente de microfone ou de alto-falante de um dispositivo Hookswitch, use **phoneSetHookSwitch** com o modo Hookswitch apropriado. A função [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) pode ser usada para consultar o modo de Hookswitch de um dispositivo Hookswitch de um dispositivo de telefone aberto.

Quando o modo do Dispositivo Hookswitch de um telefone é alterado manualmente, por exemplo, levantando o monofone de sua base, uma mensagem de [**\_ estado do telefone**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

O volume do componente de palestrante de um dispositivo Hookswitch pode ser definido com [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). A configuração de volume é diferente de mudo para ativar mudo de um orador e, mais tarde, desfazê-lo preservará a configuração do volume do orador. A função [**phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) pode ser usada para retornar a configuração de volume atual do alto-falante de um dispositivo Hookswitch de um dispositivo de telefone aberto.

O componente de microfone de um dispositivo Hookswitch também pode ser controlado. A configuração de obter é diferente de mudo para ativar mudo de um microfone e, mais tarde, desfazê-lo preservará a configuração de obter do microfone. Use [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) para definir o lucro do microfone de um dispositivo Hookswitch de um dispositivo de telefone aberto e [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) para retornar a configuração de obter do microfone de um dispositivo Hookswitch de um telefone aberto.

Quando o volume ou o controle do Dispositivo Hookswitch de um telefone é alterado, uma \_ mensagem de estado do telefone é enviada para a função do aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros dessa mensagem fornecem uma indicação da alteração.

 

 



