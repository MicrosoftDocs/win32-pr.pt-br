---
title: Habilitando STRICT
description: Ao definir o símbolo estrito, você habilita recursos que exigem mais cuidado na declaração e no uso de tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ca814d69910620b89095cc18be3b37601329dc053937d5772243097537c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561790"
---
# <a name="enabling-strict"></a>Habilitando STRICT

Ao definir o símbolo **estrito** , você habilita recursos que exigem mais cuidado na declaração e no uso de tipos. Isso ajuda a escrever código mais portátil. Esse cuidado extra também reduzirá o tempo de depuração. Habilitar **estrito** redefine determinados tipos de dados para que o compilador não permita a atribuição de um tipo para outro sem uma conversão explícita. isso é especialmente útil com Windows código. Erros na passagem de tipos de dados são relatados em tempo de compilação em vez de causar erros fatais em tempo de execução.

Com Visual C++, a verificação de tipo **estrito** é definida por padrão.

para definir **STRICT** em uma base file-by-file, insira uma instrução de **\# definição** antes de incluir Windows. h:


```C++
#define STRICT
#include <windows.h>
```



Quando **Strict** é definido, as definições de [tipo de dados](windows-data-types.md) são alteradas da seguinte maneira:

-   Tipos de identificador específicos são definidos para serem mutuamente exclusivos; por exemplo, você não poderá passar um **HWND** onde um argumento de tipo **HDC** é necessário. Sem **estrito**, todos os identificadores são definidos como **identificadores**, portanto, o compilador não impede que você use um tipo de identificador em que outro tipo é esperado.
-   Todos os tipos de função de retorno de chamada (como procedimentos de caixa de diálogo, procedimentos de janela e procedimentos de gancho) são definidos com protótipos completos. Isso impede que você declare funções de retorno de chamada com listas de parâmetros incorretas.
-   Os tipos de valor de parâmetro e de retorno que devem usar um ponteiro genérico são declarados corretamente como **LPVOID** , em vez de um **LPSTR** ou outro tipo de ponteiro.
-   A estrutura [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) é declarada de acordo com o padrão ANSI.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desabilitando estrito](disabling-strict.md)
</dt> <dt>

[Conformidade estrita](strict-compliance.md)
</dt> </dl>

 

 
