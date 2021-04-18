---
description: Para remover os contadores de desempenho de aplicativos do sistema, execute as etapas a seguir.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Excluindo contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756704"
---
# <a name="deleting-performance-counters"></a>Excluindo contadores de desempenho

Para remover os contadores de desempenho do aplicativo do sistema, execute as etapas a seguir.

1.  Use a ferramenta **Unlodctr** incluída no computador para remover os dados relacionados ao contador do registro. Observe que a chave de **desempenho** do aplicativo deve existir para que a ferramenta **Unlodctr** seja realizada com sucesso. Para obter detalhes, consulte [removendo nomes de contadores e descrições do registro](removing-counter-names-and-descriptions-from-the-registry.md).
2.  Exclua as chaves de **desempenho** e **vinculação** na chave de **Serviços** do aplicativo. Para excluir essas chaves, use o utilitário Regedt32.exe ou chame [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
