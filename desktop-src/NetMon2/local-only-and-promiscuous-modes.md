---
description: Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modos Local-Only e promíscuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753248"
---
# <a name="local-only-and-promiscuous-modes"></a>Modos Local-Only e promíscuo

Os monitores podem examinar quadros no modo somente local ou no modo promíscuo.

No modo somente local, o NPP (provedor de pacotes de rede) retorna os quadros que são enviados de ou para o computador no qual o monitor está em execução, incluindo difusões e multicast direcionados para o computador local. Embora seja limitado a quadros direcionados localmente, o modo local também é muito menos intensivo do processador.

No modo promíscuo, o monitor também pode observar o tráfego que não é direcionado para ou do computador local. A menos que o monitor tenha especificado o sinalizador \_ , \_ o MCS Create pmode não é \_ \_ necessário, na função [OnLoadingDLL](onloadingdll.md) , o serviço de controle de monitor (MCSVC) pressupõe que o monitor requer o modo promíscuo ao carregar a DLL do monitor.

 

 



