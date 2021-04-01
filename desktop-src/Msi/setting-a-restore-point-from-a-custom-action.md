---
description: As ações personalizadas não devem chamar a função SRSetRestorePoint porque isso pode fazer com que um ponto de entrada de restauração seja gravado no meio de uma instalação de Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Definindo um ponto de restauração de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091767"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Definindo um ponto de restauração de uma ação personalizada

As ações personalizadas não devem chamar a função [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) porque isso pode fazer com que um ponto de entrada de restauração seja gravado no meio de uma instalação de Windows Installer.

Para obter mais informações, consulte [pontos de restauração do sistema e o Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
