---
title: Desabilitando estrito
description: Para desabilitar a verificação de tipo estrito, defina o nome do símbolo como não \_ estrito. No Visual C/C++, você também pode especificar essa definição na linha de comando ou em um makefile especificando/DNO \_ Strict como uma opção de compilador.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636394"
---
# <a name="disabling-strict"></a>Desabilitando estrito

Para desabilitar a verificação de tipo **estrito** , defina o nome do símbolo como **não \_ estrito**. No Visual C/C++, você também pode especificar essa definição na linha de comando ou em um makefile especificando **/DNO \_ Strict** como uma opção de compilador.

Para definir **não \_ estrito** em uma base arquivo por arquivo, insira uma instrução de **\# definição** antes de incluir Windows. h:


```C++
#define NO_STRICT
#include <windows.h>
```



Para obter melhores resultados, você também deve definir o nível de aviso para mensagens de erro para pelo menos **/w3**. Isso é sempre aconselhável com aplicativos para Windows, pois uma prática de codificação que causa um aviso (por exemplo, passar o número incorreto de parâmetros) geralmente causa um erro fatal em tempo de execução se não for corrigida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando STRICT](enabling-strict.md)
</dt> <dt>

[Conformidade estrita](strict-compliance.md)
</dt> </dl>

 

 




