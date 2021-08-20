---
description: Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos de banco de dados de texto ou inteiro. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. Null nunca é um valor válido para esse tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato de inteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805624"
---
# <a name="integer-format-types"></a>Tipos de formato de inteiro

Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos de banco de dados de texto ou inteiro. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. Null nunca é um valor válido para esse tipo.

O seguinte tipo de Formato de Inteiro existe.

[Tipo de inteiro arbitrário](arbitrary-integer-type.md)

Itens configuráveis do Tipo de Formato Inteiro são usados em colunas de texto ou inteiro e, em geral, podem ser substituídos por qualquer inteiro positivo ou negativo. No entanto, itens configuráveis específicos também podem ter restrições semânticas características. Por exemplo, um item configurável específico necessário para ser um inteiro entre 0 e 100 tem e restrição semântica adicional. Essas restrições não são impostas pelo Mergemod.dll e, portanto, os autores do módulo devem estar preparados para lidar com qualquer cadeia de caracteres que atenda ao tipo de Formato inteiro especificado.

 

 



