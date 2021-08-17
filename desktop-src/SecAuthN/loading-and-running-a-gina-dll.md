---
description: Windows carrega e executa a DLL do Microsoft GINA (MSGina.dll) padrão. Para carregar uma GINA diferente, você deve alterar um valor de chave do registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Carregando e executando uma DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140949"
---
# <a name="loading-and-running-a-gina-dll"></a>Carregando e executando uma DLL GINA

Windows carrega e executa a DLL do Microsoft GINA (MSGina.dll) padrão. Para carregar uma [*Gina*](../secgloss/g-gly.md)diferente, você deve alterar o seguinte valor de chave do registro:

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

 

 
