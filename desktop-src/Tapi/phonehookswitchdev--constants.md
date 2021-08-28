---
description: As \_ constantes de sinalizador de bit PHONEHOOKSWITCHDEV descrevem vários dispositivos de e/s de áudio cada um com seu próprio Hookswitch controlável do computador.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Constantes de PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77e6b776b89adf6224d6feaef8deeef1f9f71b9888929f3aea08b5342adc1dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796746"
---
# <a name="phonehookswitchdev_-constants"></a>\_Constantes PHONEHOOKSWITCHDEV

As constantes de sinalizador de bit **PHONEHOOKSWITCHDEV \_** descrevem vários dispositivos de e/s de áudio cada um com seu próprio Hookswitch controlável do computador.

<dl> <dt>

<span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**fone de PHONEHOOKSWITCHDEV \_**
</dt> <dd> <dl> <dt>



Esse é um telefone Ear e mouthpiece padrão.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**Headset de PHONEHOOKSWITCHDEV \_**
</dt> <dd> <dl> <dt>



Este é um headset conectado ao conjunto de telefone.


</dt> </dl> </dd> <dt>

<span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ palestrante**
</dt> <dd> <dl> <dt>



Este é um loudspeaker e um microfone internos. Isso também pode ser um palestrante de suplemento conectado externamente ao conjunto de telefone.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Essas constantes são usadas na estrutura de dados [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para indicar os recursos do Dispositivo Hookswitch de um dispositivo de telefone. A estrutura [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) relata o estado dos dispositivos Hookswitch do telefone. A função [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) e [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) o usam como um parâmetro para selecionar o dispositivo de e/s do telefone.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




