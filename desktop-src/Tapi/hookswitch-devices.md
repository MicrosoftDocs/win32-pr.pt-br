---
description: Um dispositivo de telefone pode ter vários dispositivos hookswitch.
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Dispositivos Hookswitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca5c9f605731780068b9ad5a5b35d913213006c62d127e6a3b15d1ffc5fe1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013096"
---
# <a name="hookswitch-devices"></a>Dispositivos Hookswitch

Um dispositivo de telefone pode ter vários dispositivos hookswitch. Um hookswitch é a opção que conecta ou desconecta um dispositivo da linha telefônica. Em um telefone, por exemplo, essa é a opção que é ativada automaticamente quando um usuário tira o receptor do compartimento para obter um novo tom de discagem. A TAPI define três tipos de dispositivos hookswitch para um telefone: handset, speakerphone e headset. Cada dispositivo hookswitch tem um alto-falante e um componente de microfone e opera em um dos quatro modos hookswitch:

-   **Onhook** O dispositivo hookswitch está ligado e o microfone e o alto-falante estão desabilitados.
-   **Somente microfone** O dispositivo hookswitch está offhook, seu microfone está habilitado e seu locutor é mudo.
-   **Somente locutor** O dispositivo hookswitch é offhook, seu microfone é mudo e seu locutor está habilitado.
-   **Microfone e alto-falante** O dispositivo hookswitch está offhook e o microfone e o alto-falante estão habilitados.

A [**função phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) é usada para definir o modo hookswitch de um ou mais dispositivos hookswitch de um dispositivo de telefone aberto. Por exemplo, para desativar ou desativar o microfone ou o componente do alto-falante de um dispositivo **hookswitch, use phoneSetHookSwitch** com o modo hookswitch apropriado. A [**função phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) pode ser usada para consultar o modo hookswitch de um dispositivo hookswitch de um dispositivo de telefone aberto.

Quando o modo do dispositivo hookswitch de um telefone é alterado manualmente, por exemplo, ao fazer o lift-in do seu telefone, uma mensagem [**PHONE \_ STATE**](phone-state.md) é enviada ao aplicativo para notificar o aplicativo sobre a alteração de estado. Os parâmetros para essa mensagem fornecem uma indicação da alteração.

O volume do componente do locutor de um dispositivo hookswitch pode ser definido com [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume). A configuração de volume é diferente de mute, na forma como um alto-falante é muting e, posteriormente, não permutável, preservará a configuração de volume do locutor. A [**função phoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) pode ser usada para retornar a configuração de volume atual de um dispositivo hookswitch do alto-falante de um dispositivo de telefone aberto.

O componente de microfone de um dispositivo hookswitch também pode ser controlado. A configuração de ganho é diferente do mute, na forma como um microfone é muting e, posteriormente, não permutável, preservará a configuração de ganho do microfone. Use [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) para definir o ganho de um microfone do dispositivo hookswitch de um dispositivo de telefone aberto e [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) para retornar a configuração de ganho de um microfone do dispositivo hookswitch de um telefone aberto.

Quando o volume ou o ganho do dispositivo hookswitch de um telefone é alterado, uma mensagem PHONE STATE é enviada para a função de aplicativo para notificar o aplicativo sobre a alteração \_ de estado. Os parâmetros para essa mensagem fornecem uma indicação da alteração.

 

 



