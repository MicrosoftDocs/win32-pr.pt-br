---
description: Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modos Local-Only e promíscuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555886"
---
# <a name="local-only-and-promiscuous-modes"></a>Modos Local-Only e promíscuo

Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.

No modo somente local, o NPP (provedor de pacotes de rede) retorna os quadros que são enviados de ou para o computador no qual o monitor está em execução, incluindo difusões e multicast direcionados para o computador local. Embora seja limitado a quadros direcionados localmente, o modo local também é muito menos intensivo do processador.

No modo promíscuo, o monitor também pode observar o tráfego que não é direcionado para ou do computador local. A menos que o monitor tenha especificado o sinalizador \_ , \_ o MCS Create pmode não é \_ \_ necessário, na função [OnLoadingDLL](onloadingdll.md) , o serviço de controle de monitor (MCSVC) pressupõe que o monitor requer o modo promíscuo ao carregar a DLL do monitor.

 

 



