---
description: Para determinar o tipo de evento do dispositivo ao processar uma \_ mensagem do WM DEVICECHANGE, examine o parâmetro wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Tipos de evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ece6b810ba4d1310638bbfbdcdcaa7f67f79d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010189"
---
# <a name="device-event-types"></a>Tipos de evento de dispositivo

Para determinar o tipo de evento do dispositivo ao processar uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) , examine o parâmetro *wParam* . O valor de *wParam* determina o significado dos dados específicos do evento no parâmetro *lParam* . Em geral, os dados específicos do evento identificam o dispositivo e fornecem detalhes adicionais sobre o evento. O formato desses dados depende do tipo de dispositivo, mas os primeiros bytes sempre têm o mesmo formato que a estrutura [**HDR de \_ difusão \_ de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Para determinar o formato dos dados, verifique o membro **\_ DeviceType dbch** .

O sistema transmite um evento de dispositivo do tipo [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (ou seja, uma mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEARRIVAL) sempre que um dispositivo tiver sido inserido e estiver disponível para uso. Os aplicativos normalmente verificam o tipo de dispositivo e começam a usar o dispositivo imediatamente, se for apropriado.

O sistema transmite um evento de dispositivo [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) para solicitar permissão para remover um dispositivo. Para determinar se ele precisa do dispositivo, um aplicativo pode exibir uma caixa de diálogo para solicitar instruções ao usuário. Se um aplicativo determinar que ele precisa do dispositivo, ele poderá negar essa solicitação e cancelar a remoção retornando a \_ negação de consulta de difusão \_ . Se o aplicativo não precisar do dispositivo, ele deverá retornar **true**. O sistema envia imediatamente uma mensagem [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) se algum aplicativo ou driver cancelou uma solicitação anterior para remover um dispositivo.

O sistema transmite um evento de dispositivo [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) como um último aviso antes de um dispositivo ser removido. Neste ponto, o aplicativo não pode cancelar a remoção, portanto, se estiver usando o dispositivo, ele deve se preparar para a remoção a fim de evitar a perda de dados. Isso é especialmente importante quando uma conexão de rede está sendo removida. O aplicativo deve determinar se algum de seus arquivos abertos ou pipes está nessa conexão. Isso pode fazer isso comparando o identificador de recurso de rede nos dados específicos do evento da mensagem com os identificadores de recurso obtidos anteriormente para os arquivos e pipes. O sistema transmite um evento de dispositivo [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) quando um dispositivo é removido e não está mais disponível.

O sistema transmite um evento de dispositivo [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) para solicitar permissão para alterar a configuração atual (Dock ou desencaixar). Qualquer aplicativo pode retornar a \_ consulta \_ de difusão negada para negar a solicitação e cancelar a alteração. Se um aplicativo negar a solicitação, o sistema enviará uma mensagem [DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md) . Se a configuração atual tiver sido alterada, devido a um Dock ou desencaixado, o sistema enviará uma mensagem [DBT \_ ConfigChanged](dbt-configchanged.md) .

O sistema transmite um evento de dispositivo [DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md) sempre que ocorre um evento específico do dispositivo.

Os drivers podem criar seus próprios tipos de evento personalizados. Os eventos personalizados são enviados somente para aplicativos que se registraram para notificação de eventos de dispositivo em um dispositivo específico e só podem ser iniciados por drivers de modo kernel. Para obter mais informações, consulte [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 



