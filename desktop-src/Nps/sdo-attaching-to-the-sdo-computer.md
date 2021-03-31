---
title: Anexando ao computador SDO
description: Com o ponteiro de interface retornado por CoCreateInstance, chame o método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917379"
---
# <a name="attaching-to-the-sdo-computer"></a>Anexando ao computador SDO

Com o ponteiro de interface retornado por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), chame o método [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Passe **NULL** como o parâmetro para o método **Attach** . O valor **NULL** especifica que **Attach** associa o objeto de computador ao computador local. Não há suporte para a anexação a um computador remoto.

Para determinar se o computador local já está anexado, chame o método [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Consulte [anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver o código de exemplo que demonstra como anexar ao computador local.

 

 