---
description: Esse atributo é a cadeia de caracteres de texto exibida no controle .
ms.assetid: 0c4b7183-a43a-4c91-b01e-9f377500ba38
title: Atributo de controle de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 249951290e59d8e76f11cae66ab61956727068c99713ed2e5a18a40c9c9a7522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141855"
---
# <a name="text-control-attribute"></a>Atributo de controle de texto

Esse atributo é a cadeia de caracteres de texto exibida no controle . Na configuração, se o campo 0 do registro não for nulo, o registro será formatado usando FormatText. Se o campo 0 for nulo, o primeiro campo do registro definirá o texto. Ao obter o valor, sempre é retornado no primeiro campo. Para alguns controles, esse texto pode não estar visível. No Windows a tecla de acelerador para um controle é definida colocando um "&" na frente do caractere desejado nessa cadeia de caracteres.

## <a name="valid-controls"></a>Controles válidos

Todos os controles, exceto o [Controle de Linha](line-control.md).

## <a name="associated-bit-flags"></a>Sinalizadores de bit associados

Nenhum.

## <a name="remarks"></a>Comentários

Consulte [Atributos de controle](control-attributes.md) e o controle que você precisa criar em [Controles](controls.md).

 

 



