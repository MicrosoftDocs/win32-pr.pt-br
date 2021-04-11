---
description: A \_ Propriedade PKEY AudioEndpoint \_ Disable \_ SysFx especifica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089451"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ Disable \_ SysFx

A propriedade **PKEY \_ AudioEndpoint \_ Disable \_ SysFx** especifica se os efeitos do sistema estão habilitados no fluxo de modo compartilhado que flui para ou do dispositivo de ponto de extremidade de áudio.

Os efeitos do sistema são implementados como objetos de processamento de áudio (APOs) que podem ser inseridos em um fluxo de áudio. APOs são módulos de software que executam funções de processamento de áudio, como controle de volume e conversão de formato. A desabilitação dos efeitos do sistema para um dispositivo de ponto de extremidade permite que o fluxo associado passe pelo APOs não modificado.

Para obter mais informações sobre os efeitos do sistema no Windows Vista, consulte os White papers intitulados "efeitos de áudio personalizados no Windows Vista" e "reutilizando os efeitos do sistema de áudio do Windows Vista" no site de [tecnologias do dispositivo de áudio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Essa propriedade aplica-se somente aos efeitos locais e aos efeitos globais APOs que foram instalados pelo arquivo. inf que instalou o adaptador de áudio ao qual o dispositivo de ponto de extremidade está conectado. Além disso, essa propriedade afeta apenas o dispositivo de ponto de extremidade de destino — ele não tem nenhum efeito sobre os efeitos do sistema para nenhum outro dispositivo de ponto de extremidade, mesmo se eles se conectarem ao mesmo adaptador.

O membro **VT** da estrutura **PROPVARIANT** é definido como **VT \_ UI4**.

O membro **ulVal** da estrutura **PROPVARIANT** é definido como **Endpoint \_ SYSFX \_ habilitado** se os efeitos do sistema estiverem habilitados ou o ponto de **extremidade \_ SYSFX \_ desabilitado** se eles estiverem desabilitados.

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

 

 




