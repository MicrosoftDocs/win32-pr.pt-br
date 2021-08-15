---
title: Considerações de segurança sistema de cores do Windows
description: Considerações de segurança sistema de cores do Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Sistema de Cores (WCS), segurança
- WCS (Windows color system),segurança
- gerenciamento de cores da imagem, segurança
- gerenciamento de cores, segurança
- segurança para Windows sistema de cores (WCS)
- CmM (Módulo de Gerenciamento de Cores)
- CMM (Módulo de Gerenciamento de Cores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444663"
---
# <a name="security-considerations-windows-color-system"></a>Considerações sobre segurança: Windows de cores

Este documento fornece informações sobre considerações de segurança relacionadas ao gerenciamento de cores da imagem. Este documento não fornece tudo o que você precisa saber sobre problemas de segurança– em vez disso, use-o como um ponto de partida e uma referência para essa área de tecnologia.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>CmMs não Microsoft podem ser executados no contexto do sistema

CmMs (Módulos de Gerenciamento de Cores) não Microsoft devem ser tratados como drivers de impressora não Microsoft, pois eles têm o potencial de serem executados em um contexto do sistema para operações de impressão.
