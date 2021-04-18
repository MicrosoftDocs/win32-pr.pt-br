---
description: As ações personalizadas são invocadas da mesma maneira que as ações padrão, seja por invocação explícita ou durante a execução de uma tabela de sequência.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Invocando ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758623"
---
# <a name="invoking-custom-actions"></a>Invocando ações personalizadas

As ações personalizadas são invocadas da mesma maneira que as ações padrão, seja por invocação explícita ou durante a execução de uma tabela de sequência. Há dois métodos para chamar ações:

-   Você chama a ação especificada diretamente com a função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .
-   Uma ação de nível superior chama a tabela de sequência que contém a ação personalizada. Para obter mais informações sobre como agendar uma ação personalizada em uma tabela de sequência, consulte [sequenciando ações personalizadas](sequencing-custom-actions.md).

Quando o instalador obtém um nome de ação da função [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou de uma tabela de sequência, ele primeiro procura uma ação padrão desse nome. Se não for possível localizar a ação padrão, o instalador consultará a [tabela CustomAction](customaction-table.md) para verificar se a ação especificada é uma ação personalizada. Se a ação especificada não for uma ação personalizada, o instalador consultará a [tabela de diálogo](dialog-table.md) em busca de uma caixa de diálogo.

 

 



