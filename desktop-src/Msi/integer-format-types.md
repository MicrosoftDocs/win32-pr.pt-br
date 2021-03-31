---
description: Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos texto ou banco de dados inteiro. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. NULL nunca é um valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato de inteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662333"
---
# <a name="integer-format-types"></a>Tipos de formato de inteiro

Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos texto ou banco de dados inteiro. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. NULL nunca é um valor válido para este tipo.

O tipo de formato inteiro a seguir existe.

[Tipo de inteiro arbitrário](arbitrary-integer-type.md)

Os itens configuráveis do tipo de formato inteiro são usados em colunas de texto ou de inteiro e, em geral, podem ser substituídos por qualquer inteiro positivo ou negativo. No entanto, determinados itens configuráveis também podem ter restrições semânticas de características. Por exemplo, um item configurável específico necessário para ser um inteiro entre 0 e 100 tem uma restrição semântica adicional. Essas restrições não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato inteiro especificado.

 

 



