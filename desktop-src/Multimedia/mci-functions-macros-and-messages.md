---
title: Macros e mensagens de funções MCI
description: Macros e mensagens de funções MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Mensagens MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b411c018c55254658972d3cdc21a9d721334d5e78635b38f636892e2c80797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784316"
---
# <a name="mci-functions-macros-and-messages"></a>Macros e mensagens de funções MCI

A maioria dos aplicativos MCI usa as [**funções mciSendString**](/previous-versions//dd757161(v=vs.85)) e [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) dezenas de vezes. A MCI fornece algumas outras funções úteis que seu aplicativo usará com menos frequência.

O identificador de dispositivo exigido pela maioria dos comandos MCI normalmente é recuperado em uma chamada para o comando [**open**](open.md) ([**MCI \_ OPEN**](mci-open.md)). Se você precisar de um identificador de dispositivo, mas não quiser abrir o dispositivo , por exemplo, se quiser consultar os recursos do dispositivo antes de tomar qualquer outra ação, poderá chamar a [**função mciGetDeviceID.**](/previous-versions//dd757156(v=vs.85))

A [**função mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) permite que seu aplicativo use um identificador de dispositivo para recuperar um identificador para a tarefa que criou esse identificador.

Você pode usar as funções [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) e [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) para atribuir e recuperar o endereço da função de retorno de chamada associada ao sinalizador "wait" (MCI \_ WAIT).

A [**função mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera uma cadeia de caracteres que descreve um valor de erro MCI. Cada cadeia de caracteres retornada pela MCI, seja dados ou uma descrição de erro, tem um máximo de 128 caracteres. Os campos da caixa de diálogo menores que 128 caracteres truncarão as cadeias de caracteres mais longas retornadas pela MCI. Para obter mais informações sobre essas cadeias de caracteres, consulte [Valores de retorno mcierr](mcierr-return-values.md).

As macros MCI são ferramentas que você pode usar para criar e desmontar valores que especificam formatos de hora. Esses formatos de hora são usados em muitos comandos MCI. Os formatos agidos pelas macros são HORAS/minutos/segundos (HMS), minutos/segundos/quadros (MSF) e faixas/minutos/segundos/quadros (TMSF). A tabela a seguir lista as macros e suas descrições.



| Macro                                        | Descrição                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ HOUR**](mci-hms-hour.md)       | Recupera o componente hours de um valor HMS.   |
| [**MCI \_ HMS \_ MINUTE**](mci-hms-minute.md)   | Recupera o componente minutes de um valor HMS. |
| [**MCI \_ HMS \_ SECOND**](mci-hms-second.md)   | Recupera o componente seconds de um valor HMS. |
| [**MCI \_ MAKE \_ HMS**](mci-make-hms.md)       | Cria um valor DE HMS.                              |
| [**MCI \_ MAKE \_ MSF**](mci-make-msf.md)       | Cria um valor MSF.                              |
| [**MCI \_ MAKE \_ TMSF**](mci-make-tmsf.md)     | Cria um valor TMSF.                              |
| [**MCI \_ MSF \_ FRAME**](/previous-versions//dd743438(v=vs.85))     | Recupera o componente quadros de um valor MSF.  |
| [**MCI \_ MSF \_ MINUTE**](mci-msf-minute.md)   | Recupera o componente minutes de um valor MSF. |
| [**MCI \_ MSF \_ SECOND**](mci-msf-second.md)   | Recupera o componente seconds de um valor MSF. |
| [**MCI \_ TMSF \_ FRAME**](mci-tmsf-frame.md)   | Recupera o componente frames de um valor TMSF.  |
| [**MCI \_ TMSF \_ MINUTE**](mci-tmsf-minute.md) | Recupera o componente minutes de um valor TMSF. |
| [**MCI \_ TMSF \_ SECOND**](mci-tmsf-second.md) | Recupera o componente seconds de um valor TMSF. |
| [**MCI \_ TMSF \_ TRACK**](mci-tmsf-track.md)   | Recupera o componente de faixas de um valor TMSF.  |



 

A MCI também fornece duas mensagens: [**MM \_ MCINOTIFY**](mm-mcinotify.md) e [**MM \_ MCISIGNAL.**](mm-mcisignal.md) A mensagem MM MCINOTIFY notifica um aplicativo do resultado de um comando MCI sempre que esse comando especifica o sinalizador \_ "notify" (MCI \_ NOTIFY). A mensagem MM MCISIGNAL é específica para dispositivos de vídeo digital; ela notifica o aplicativo \_ quando uma posição especificada é atingida.

 

 