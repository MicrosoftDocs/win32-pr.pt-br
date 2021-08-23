---
description: O \_ \_ Mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764286"
---
# <a name="__msipromptforcd-mutex"></a>\_\_MsiPromptForCD Mutex

O \_ \_ Mutex MsiPromptForCD existe quando o instalador solicita que o usuário insira um CD-ROM. Programas de reprodução automática devem verificar se o \_ \_ mutex MsiPromptForCD não está definido no momento antes de iniciar. Observe que é possível que um prompt de CD-ROM ocorra antes que a chave InProgress ou o \_ Mutex MSIExecute exista.

 

 



