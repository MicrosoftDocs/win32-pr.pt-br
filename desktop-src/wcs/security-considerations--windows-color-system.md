---
title: Considerações de segurança sistema de cores do Windows
description: Considerações de segurança sistema de cores do Windows
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- WCS (sistema de cores do Windows), segurança
- WCS (sistema de cores do Windows), segurança
- gerenciamento de cores de imagem, segurança
- gerenciamento de cores, segurança
- segurança para o WCS (sistema de cores do Windows)
- Módulo de gerenciamento de cores (CMM)
- CMM (módulo de gerenciamento de cores)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105766591"
---
# <a name="security-considerations-windows-color-system"></a><span data-ttu-id="5b2ea-110">Considerações de segurança: sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="5b2ea-110">Security Considerations: Windows Color System</span></span>

<span data-ttu-id="5b2ea-111">Este documento fornece informações sobre considerações de segurança relacionadas ao gerenciamento de cores de imagem.</span><span class="sxs-lookup"><span data-stu-id="5b2ea-111">This document provides information about security considerations related to image color management.</span></span> <span data-ttu-id="5b2ea-112">Este documento não fornece tudo o que você precisa saber sobre problemas de segurança. em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.</span><span class="sxs-lookup"><span data-stu-id="5b2ea-112">This document doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

## <a name="non-microsoft-cmms-can-run-in-system-context"></a><span data-ttu-id="5b2ea-113">CMMs não Microsoft podem ser executados no contexto do sistema</span><span class="sxs-lookup"><span data-stu-id="5b2ea-113">Non-Microsoft CMMs can run in system context</span></span>

<span data-ttu-id="5b2ea-114">Os CMMs (módulos de gerenciamento de cores que não são da Microsoft) devem ser tratados como drivers de impressora não Microsoft porque eles têm o potencial de execução em um contexto do sistema para operações de impressão.</span><span class="sxs-lookup"><span data-stu-id="5b2ea-114">Non-Microsoft Color Management Modules (CMMs) should be treated like non-Microsoft printer drivers because they have the potential to run in a system context for printing operations.</span></span>
