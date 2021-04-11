---
title: Habilitando informações de erro estendidas
description: Habilitando informações de erro estendidas para RPC (chamada de procedimento remoto).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160071"
---
# <a name="enabling-extended-error-information"></a>Habilitando informações de erro estendidas

Para habilitar as informações de erro estendidas, execute as seguintes etapas:

Abra a política do computador local usando a interface gpedit. msc.

Navegue até a política localizada em configuração do computador/Modelos Administrativos/sistema/chamada de procedimento remoto/suporte para solução de problemas de RPC/propagação de informações de erro estendidas

Habilite a política e defina a **propagação de campo de informações de erro estendidas** como "ativadas".

Esse processo ativa a propagação de informações de erro estendidas para todos os processos no computador.

Para habilitar informações de erro estendidas para apenas determinados processos em um computador ou para desabilitá-lo somente para determinados processos no computador, use as opções **desativar com exceções** ou **com exceções** . As duas opções usam as **exceções de informações de erro estendidas** do campo para especificar quais processos têm a configuração padrão e quais processos têm o oposto da configuração padrão. **Exceções de informações de erro estendidas** contém uma lista de nomes de processo.

Se a linha de comando de um processo começar com uma cadeia de caracteres que está nas **exceções de informações de erro estendidas**, o processo receberá o oposto da configuração padrão. Por exemplo, se você quiser que todo o processo em seu computador propague informações de erro estendidas, exceto para LSASS e o processo chamado **servidor seguro**, defina a **propagação de informações de erro estendidas** como **ativado com exceções** e especifique no campo **exceções de informações de erro estendidas** a seguinte cadeia de caracteres: lsass "servidor seguro".

As cadeias de caracteres podem ser colocadas entre aspas duplas, mas isso é opcional se não houver nenhum espaço na cadeia de caracteres. Além disso, o início da linha de comando do processo pode ser especificado. Por exemplo, se a **opção desativado com exceções** for especificada no campo **propagação de informações de erro estendidas** e no campo **exceções de informações de erro estendidas** , o seguinte será especificado: Win.

Cada processo que começa com "win" propaga informações de erro estendidas. Em muitos computadores, por exemplo, esses processos seriam winlogon.exe e WINWORD.EXE.

 

 




