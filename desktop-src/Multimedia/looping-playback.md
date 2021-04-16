---
title: Reprodução de loop para MCIWnd
description: Reprodução de looping (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188007"
---
# <a name="looping-playback-for-mciwnd"></a>Reprodução de loop para MCIWnd

O MCIWnd dá suporte à reprodução como um loop contínuo. Você pode reproduzir o conteúdo de um arquivo ou dispositivo repetidamente como um loop usando a macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) em combinação com o botão **reproduzir** na barra de ferramentas. O dispositivo de reprodução de vídeo, MCIAVI, dá suporte a loops de reprodução. Para determinar se a reprodução contínua foi ativada, use a macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




