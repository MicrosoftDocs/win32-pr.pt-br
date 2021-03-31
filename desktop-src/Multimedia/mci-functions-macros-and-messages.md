---
title: Mensagens e macros de funções MCI
description: Mensagens e macros de funções MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Mensagens MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641023"
---
# <a name="mci-functions-macros-and-messages"></a>Mensagens e macros de funções MCI

A maioria dos aplicativos MCI usa as funções [**mciSendString**](/previous-versions//dd757161(v=vs.85)) e [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) dezenas de vezes. O MCI fornece algumas outras funções úteis que seu aplicativo usará com menos frequência.

O identificador de dispositivo exigido pela maioria dos comandos MCI é normalmente recuperado em uma chamada para o comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Se você precisar de um identificador de dispositivo, mas não quiser abrir o dispositivo — por exemplo, se desejar consultar os recursos do dispositivo antes de realizar qualquer outra ação — você pode chamar a função [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .

A função [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) permite que seu aplicativo use um identificador de dispositivo para recuperar um identificador para a tarefa que criou esse identificador.

Você pode usar as funções [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) e [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) para atribuir e recuperar o endereço da função de retorno de chamada associada ao sinalizador "Wait" (espera de MCI \_ ).

A função [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera uma cadeia de caracteres que descreve um valor de erro MCI. Cada cadeia de caracteres que o MCI retorna, se os dados ou uma descrição de erro, têm um máximo de 128 caracteres. Os campos de caixa de diálogo menores que 128 caracteres truncarão as cadeias mais longas retornadas pelo MCI. Para obter mais informações sobre essas cadeias de caracteres, consulte [MCIERR Return Values](mcierr-return-values.md).

As macros MCI são ferramentas que você pode usar para criar e desmontar valores que especificam formatos de hora. Esses formatos de hora são usados em muitos comandos MCI. Os formatos acionados pelas macros são horas/minutos/segundos (HMS), minutos/segundos/quadros (MSF) e faixas/minutos/segundos/quadros (TMSF). A tabela a seguir lista as macros e suas descrições.



| Macro                                        | Descrição                                        |
|----------------------------------------------|----------------------------------------------------|
| [**\_hora de HMS MCI \_**](mci-hms-hour.md)       | Recupera o componente de horas de um valor de HMS.   |
| [**\_HMS \_ minutos MCI**](mci-hms-minute.md)   | Recupera o componente de minutos de um valor HMS. |
| [**MCI \_ HMS \_ segundo**](mci-hms-second.md)   | Recupera o componente de segundos de um valor de HMS. |
| [**\_HMS de make MCI \_**](mci-make-hms.md)       | Cria um valor de HMS.                              |
| [**\_criar \_ MSF do MCI**](mci-make-msf.md)       | Cria um valor de MSF.                              |
| [**\_TMSF de make MCI \_**](mci-make-tmsf.md)     | Cria um valor de TMSF.                              |
| [**\_quadro do MSF do MCI \_**](/previous-versions//dd743438(v=vs.85))     | Recupera o componente frames de um valor MSF.  |
| [**\_minuto do MSF do MCI \_**](mci-msf-minute.md)   | Recupera o componente de minutos de um valor do MSF. |
| [**MSF do MCI \_ \_ segundo**](mci-msf-second.md)   | Recupera o componente de segundos de um valor do MSF. |
| [**\_quadro TMSF \_ MCI**](mci-tmsf-frame.md)   | Recupera o componente frames de um valor TMSF.  |
| [**\_TMSF \_ minutos MCI**](mci-tmsf-minute.md) | Recupera o componente de minutos de um valor TMSF. |
| [**MCI \_ TMSF \_ segundo**](mci-tmsf-second.md) | Recupera o componente de segundos de um valor de TMSF. |
| [**\_faixa de TMSF MCI \_**](mci-tmsf-track.md)   | Recupera o componente trilhas de um valor TMSF.  |



 

O MCI também fornece duas mensagens: [**mm \_ MCINOTIFY**](mm-mcinotify.md) e [**mm \_ MCISIGNAL**](mm-mcisignal.md). A \_ mensagem mm MCINOTIFY notifica um aplicativo sobre o resultado de um comando MCI sempre que esse comando especifica o sinalizador "notificar" ( \_ notificação MCI). A \_ mensagem mm MCISIGNAL é específica para dispositivos de vídeo digital; ela notifica o aplicativo quando uma posição especificada é atingida.

 

 