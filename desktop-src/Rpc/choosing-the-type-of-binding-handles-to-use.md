---
title: Escolhendo o tipo de identificador de associação a ser usado
description: Escolhendo o tipo de identificador de associação a ser usado
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd35286a5bb88be3094238e0e4c43b701826bca0a7e5ad02d35c5f87f0cbdaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022916"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Escolhendo o tipo de identificador de associação a ser usado

**Melhor prática:** Se você sabe qual servidor o aplicativo usará, use alças explícitas. Caso não, use a construção de alças explícitas toda vez ou use alças genéricas com rotinas **\_ de** vinculação e desavinculação. **\_**

Não use alças implícitas ou alças automáticas. Os alças implícitos não são thread-safe e, embora o thread safety possa parecer desnecessário, isso pode se tornar necessário mais tarde. Os alças automáticos têm uma grande sobrecarga e exigem muita configuração para funcionar corretamente. Suas funcionalidades de pesquisa foram superadas pelos serviços do Active Directory.

Os alças explícitos são altamente eficientes e muitos recursos atraentes estão disponíveis apenas para alças explícitas. Por exemplo, se várias chamadas RPC vão para o mesmo servidor, você pode construir o alça de associação uma vez e fazer todas as chamadas com ele. Essa abordagem é muito mais eficiente do que qualquer outro método. Se o servidor para o qual a chamada será feita for desconhecido, construa um identificador de associação explícito para cada chamada ou use identificador de associação genérico.

No Microsoft™ Windows XP, o tempo de execução de RPC é bastante eficiente em reajustar e armazenar em cache chamadas, portanto, se a *n*+1ª chamada terminar no mesmo servidor que a *nª* chamada, o RPC re-usa os recursos alocados para a nª chamada, contornando a necessidade de cache de alças de associação para melhorar o desempenho. 

 

 




