---
description: É altamente recomendável que você execute a validação em cada pacote de instalação novo ou recém modificado antes de tentar instalar o pacote pela primeira vez.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Validação do pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827870"
---
# <a name="package-validation"></a>Validação do pacote

É altamente recomendável que você execute a validação em cada pacote de instalação novo ou recém modificado antes de tentar instalar o pacote pela primeira vez.

A validação do pacote inclui os três processos a seguir:

-   [Validação interna](internal-validation.md)
-   [Validação do pool de cadeias de caracteres](string-pool-validation.md)
-   [Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)

Os módulos de mesclagem devem ser validados usando o método descrito em [Validando módulos de mesclagem](validating-merge-modules.md).

Evalcom2.dll fornece um objeto COM que implementa operações de validação para pacotes de instalação e módulos de mesclagem. O objeto principal implementa interfaces para programas C/C++. Para obter mais informações, consulte [automação de validação](validation-automation.md).

 

 



