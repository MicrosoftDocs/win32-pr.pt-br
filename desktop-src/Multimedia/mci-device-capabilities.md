---
title: Recursos do dispositivo MCI
description: Recursos do dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Macro MCIWndCanConfig
- Macro MCIWndCanEject
- Macro MCIWndCanPlay
- Macro MCIWndCanRecord
- Macro MCIWndCanSave
- Macro MCIWndCanWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006069"
---
# <a name="mci-device-capabilities"></a>Recursos do dispositivo MCI

O MCIWnd inclui as macros a seguir para permitir que você consulte os dispositivos MCI para obter seus recursos.



| Macro                                      | Descrição                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Determina se um dispositivo tem uma caixa de diálogo de configuração para dar suporte a várias configurações, como o dispositivo MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Determina se um dispositivo tem uma função de ejeção controlada por software.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Determina se um dispositivo pode reproduzir o conteúdo existente.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Determina se um dispositivo pode gravar.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Determina se um dispositivo pode armazenar dados.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Determina se um dispositivo dá suporte a comandos de janela MCI (como [**janela**](window.md), [**Put**](put.md) e [**Where**](where.md)). |



 

Essas macros retornarão **true** se o dispositivo der suporte à capacidade específica ou **false** caso contrário.

 

 




