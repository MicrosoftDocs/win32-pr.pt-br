---
title: Desabilitando STRICT
description: Para desabilitar a verificação de tipo STRICT, defina o nome do símbolo NO \_ STRICT. No Visual C/C++, você também pode especificar essa definição na linha de comando ou em um makefile especificando /DNO STRICT como uma opção \_ do compilador.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078361b5cc3fd4916ac2ab4f7207752e869568b8781c9ef3dd8e38427d252592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743652"
---
# <a name="disabling-strict"></a>Desabilitando STRICT

Para desabilitar a verificação de tipo **STRICT,** defina o nome do símbolo **NO \_ STRICT.** No Visual C/C++, você também pode especificar essa definição na linha de comando ou em um makefile especificando **/DNO \_ STRICT** como uma opção do compilador.

Para definir **NO \_ STRICT** em uma base de arquivo por arquivo, insira uma instrução **\# define** antes de incluir Windows.h:


```C++
#define NO_STRICT
#include <windows.h>
```



Para melhores resultados, você também deve definir o nível de aviso para mensagens de erro como pelo menos **/W3**. Isso é sempre aconselhável com aplicativos para Windows, porque uma prática de codificação que causa um aviso (por exemplo, passar o número errado de parâmetros) geralmente causa um erro fatal em tempo de executar se ele não for corrigido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando STRICT](enabling-strict.md)
</dt> <dt>

[Conformidade ESTRITA](strict-compliance.md)
</dt> </dl>

 

 




