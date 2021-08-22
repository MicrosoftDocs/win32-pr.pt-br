---
description: Os tipos de formato bitfield de dados configuráveis podem ser usados em campos de banco de dados inteiros.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Tipos de formato bitfield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6f4052df6780d88397aa26da66ac9db3755e80cffd70efb642cc5873d216d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145729"
---
# <a name="bitfield-format-types"></a>Tipos de formato bitfield

Os tipos de formato bitfield de dados configuráveis podem ser usados em campos de banco de dados inteiros. O usuário deve escolher um valor de um subconjunto especificado. Isso é apenas por convenção e não é imposto por Mergemod.dll. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. Null nunca é um valor válido para esse tipo.

O seguinte tipo de Formato bitfield existe.

[Tipo de bitfield arbitrário](arbitrary-bitfield-type.md)

Itens configuráveis do Tipo de Formato bitfield são usados em colunas inteiras e, em geral, podem ser substituídos por qualquer inteiro. O usuário deve escolher um valor de um subconjunto especificado. Isso é apenas por convenção, no entanto, e não é imposto por Mergemod.dll. O autor deve preparar o módulo para lidar com qualquer valor.

 

 



