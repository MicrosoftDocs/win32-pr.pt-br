---
description: É altamente recomendável que você execute a validação em cada pacote de instalação novo ou modificado recentemente antes de tentar instalar o pacote pela primeira vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validação de pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2fb8fe877f68a1c787458e7703fb59f035031fc68bba1d75f24e86851aac7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074846"
---
# <a name="package-validation"></a>Validação de pacote

É altamente recomendável que você execute a validação em cada pacote de instalação novo ou modificado recentemente antes de tentar instalar o pacote pela primeira vez.

A validação de pacote inclui os três processos a seguir:

-   [Validação interna](internal-validation.md)
-   [Validação do pool de cadeias de caracteres](string-pool-validation.md)
-   [Avaliadores de consistência interna – ICEs](internal-consistency-evaluators-ices.md)

Os módulos de mesclagem devem ser validados usando o método descrito em [Validando módulos de mesclagem.](validating-merge-modules.md)

Evalcom2.dll fornece um objeto COM que implementa operações de validação para pacotes de instalação e módulos de mesclagem. O objeto principal implementa interfaces para programas C/C++. Para obter mais informações, consulte [Validation Automation](validation-automation.md).

 

 



