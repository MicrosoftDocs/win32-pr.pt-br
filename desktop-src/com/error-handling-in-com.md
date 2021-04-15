---
title: Tratamento de erro no COM (COM)
description: Tratamento de erro em COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454577"
---
# <a name="error-handling-in-com-com"></a>Tratamento de erro no COM (COM)

Quase todas as funções COM e métodos de interface retornam um valor do tipo **HRESULT**. O **HRESULT** (para o *identificador de resultado*) é uma maneira de retornar valores de êxito, de aviso e de erro. **HRESULT** s não são realmente identificadores para nada; Eles são apenas valores com vários campos codificados no valor. De acordo COM a especificação COM, um resultado de zero indica êxito e um resultado diferente de zero indica falha.

No nível do código-fonte, todos os valores de erro consistem em três partes, separadas por sublinhados. A primeira parte é o prefixo que identifica o recurso associado ao erro, a segunda parte é E para erro e a terceira parte é uma cadeia de caracteres que descreve a condição real. Por exemplo, **STG \_ E \_ MEDIUMFULL** é retornado quando não há nenhum espaço restante em um disco rígido. O prefixo **STG** indica o recurso de armazenamento, o **E** indica que o código de status representa um erro e o **MEDIUMFULL** fornece informações específicas sobre o erro. Muitos dos valores que você pode querer retornar de um método ou função de interface são definidos em Winerror. h.

Para obter mais informações sobre o tratamento de erros, consulte as seguintes seções:

-   [Estrutura de códigos de erro COM](structure-of-com-error-codes.md)
-   [Códigos no FACILITy \_ ITF](codes-in-facility-itf.md)
-   [Usando macros para tratamento de erro](using-macros-for-error-handling.md)
-   [Tratamento de erro COM em Java e Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Estratégias de tratamento de erros](error-handling-strategies.md)
-   [Manipulando erros desconhecidos](handling-unknown-errors.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de erro COM](com-error-codes.md)
</dt> </dl>

 

 




