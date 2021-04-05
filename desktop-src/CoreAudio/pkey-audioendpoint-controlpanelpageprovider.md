---
description: A \_ Propriedade PKEY AudioEndpoint \_ ControlPanelPageProvider especifica o CLSID do provedor registrado da extensão de propriedades de dispositivo para o dispositivo de ponto de extremidade de áudio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826406"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

A propriedade **PKEY \_ AudioEndpoint \_ CONTROLPANELPAGEPROVIDER** especifica o CLSID do provedor registrado da extensão de propriedades de dispositivo para o dispositivo de ponto de extremidade de áudio. A extensão fornece as propriedades do ponto de extremidade de áudio que são exibidas na página de propriedades do dispositivo do painel de controle multimídia do Windows, Mmsys.cpl. Para obter mais informações sobre Mmsys.cpl, consulte a documentação do Windows DDK.

O membro **VT** da estrutura **PROPVARIANT** é definido como VT \_ LPWSTR.

O membro **pwszVal** da estrutura **PROPVARIANT** aponta para uma cadeia de caracteres largos terminada em nulo que contém um GUID que identifica o provedor da extensão do painel de controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades do ponto de extremidade de áudio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriedades de áudio de núcleo](core-audio-properties.md)
</dt> </dl>

 

 




