---
description: Para determinar se um contador está instalado em um computador específico, chame PdhValidatePath com o caminho do contador totalmente qualificado. A função retornará êxito de erro \_ se o contador estiver localizado no computador especificado.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Determinando se um contador está localizado em um computador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2cc6672125f961fc2759d264caa6c33ab68f46347c915e82d1666f667692fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061194"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a>Determinando se um contador está localizado em um computador

Para determinar se um contador está instalado em um computador específico, chame [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) com o caminho do contador totalmente qualificado. A função retornará êxito de erro \_ se o contador estiver localizado no computador especificado.

[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) valida o caminho inteiro; Portanto, se qualquer objeto, instância ou contador no caminho não existir, o valor de retorno indicará isso. **PdhValidatePath** verifica o caminho do contador especificado nesta ordem: computador, objeto de desempenho, instância e contador.

 

 



