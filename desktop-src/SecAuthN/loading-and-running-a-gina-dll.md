---
description: O Windows carrega e executa a DLL padrão do Microsoft GINA (MSGina.dll). Para carregar uma GINA diferente, você deve alterar um valor de chave do registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Carregando e executando uma DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747510"
---
# <a name="loading-and-running-a-gina-dll"></a>Carregando e executando uma DLL GINA

O Windows carrega e executa a DLL padrão do Microsoft GINA (MSGina.dll). Para carregar uma [*Gina*](../secgloss/g-gly.md)diferente, você deve alterar o seguinte valor de chave do registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Se o valor da chave GinaDLL estiver presente, ele deverá conter o nome de uma DLL GINA, que o [*Winlogon*](../secgloss/w-gly.md) carregará e usará.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando e testando uma DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Funções de exportação GINA](authentication-functions.md)
</dt> <dt>

[Estruturas GINA](authentication-structures.md)
</dt> <dt>

[Funções de GINA de serviços de terminal](terminal-services-gina-functions.md)
</dt> </dl>

 

 
