---
title: Anexando ao computador SDO
description: Com o ponteiro de interface retornado por CoCreateInstance, chame o método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362184"
---
# <a name="attaching-to-the-sdo-computer"></a>Anexando ao computador SDO

Com o ponteiro de interface retornado por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), chame o método [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) . Passe **NULL** como o parâmetro para o método **Attach** . O valor **NULL** especifica que **Attach** associa o objeto de computador ao computador local. Não há suporte para a anexação a um computador remoto.

Para determinar se o computador local já está anexado, chame o método [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .

Consulte [anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver o código de exemplo que demonstra como anexar ao computador local.

 

 