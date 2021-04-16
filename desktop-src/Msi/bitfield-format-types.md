---
description: Os tipos de formato de campo de bits de dados configuráveis podem ser usados em campos de banco de dado inteiro.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Tipos de formato de campo de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b443f7ee363d1a2b48eb580623018264df8d50be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757530"
---
# <a name="bitfield-format-types"></a>Tipos de formato de campo de bits

Os tipos de formato de campo de bits de dados configuráveis podem ser usados em campos de banco de dado inteiro. O usuário deve escolher um valor de um subconjunto especificado. Isso é apenas por convenção e não é imposto por Mergemod.dll. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. NULL nunca é um valor válido para este tipo.

O seguinte tipo de formato de campo de bits existe.

[Tipo de campo de bits arbitrário](arbitrary-bitfield-type.md)

Os itens configuráveis do tipo de formato de campo de bits são usados em colunas de inteiros e, em geral, podem ser substituídos por qualquer inteiro. O usuário deve escolher um valor de um subconjunto especificado. No entanto, isso só ocorre por convenção e não é imposto por Mergemod.dll. O autor deve preparar o módulo para lidar com qualquer valor.

 

 



