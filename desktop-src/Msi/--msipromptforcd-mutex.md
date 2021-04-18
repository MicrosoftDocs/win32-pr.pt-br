---
description: O \_ \_ mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766882"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Mutex MsiPromptForCD

O \_ \_ mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM. Os programas de reprodução automática devem verificar se o \_ \_ mutex MsiPromptForCD não está definido no momento antes de iniciar. Observe que é possível que um prompt de CD-ROM ocorra antes que a chave InProgress ou o \_ mutex MSIExecute existam.

 

 



