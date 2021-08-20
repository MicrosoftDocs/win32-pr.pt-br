---
title: Reprodução de loop para MCIWnd
description: Reprodução de looping (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9144cd17886ff9d6f59bc38311481335a9ae581e5464d7feda0e7fd1a4ec2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139287"
---
# <a name="looping-playback-for-mciwnd"></a>Reprodução de loop para MCIWnd

O MCIWnd dá suporte à reprodução como um loop contínuo. Você pode reproduzir o conteúdo de um arquivo ou dispositivo repetidamente como um loop usando a macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) em combinação com o botão **reproduzir** na barra de ferramentas. O dispositivo de reprodução de vídeo, MCIAVI, dá suporte a loops de reprodução. Para determinar se a reprodução contínua foi ativada, use a macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




