---
title: Selecionando objetos filho
description: Os clientes chamam o método accSelect IAccessible para modificar a seleção ou o foco do teclado entre os filhos em um objeto. As constantes SELFLAG especificadas com a chamada definem a operação a ser executada.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291917"
---
# <a name="selecting-child-objects"></a>Selecionando objetos filho

Os clientes chamam o método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para modificar a seleção ou o foco do teclado entre os filhos em um objeto. As [constantes SELFLAG](selflag.md) especificadas com a chamada definem a operação a ser executada.

Se [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) for chamado com o sinalizador [**SELFLAG \_ TAKEFOCUS**](selflag.md) em um objeto filho que tem um **HWND**, o sinalizador terá efeito somente se o pai do objeto tiver o foco.

## <a name="performing-complex-selection-operations"></a>Executando operações de seleção complexas

O seguinte descreve quais valores de SELFLAG especificar ao chamar [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para executar operações de seleção complexas.

**Para simular um clique**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**Para selecionar um item de destino simulando CTRL + clique**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ addseleções**](selflag.md)

**Para cancelar a seleção de um item de destino simulando CTRL + clique**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**Para simular SHIFT + clique**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**Para selecionar um intervalo de objetos e colocar o foco no último objeto**

1.  Especifique [**SELFLAG \_ TAKEFOCUS**](selflag.md) no objeto inicial para definir a âncora de seleção.
2.  Chame [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) novamente e especifique [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) no último objeto.

**Para desmarcar todos os objetos**

1.  Especifique [**SELFLAG \_ TAKESELECTION**](selflag.md) em qualquer objeto. Esse sinalizador anula a seleção de todos os objetos selecionados, exceto aquele selecionado.
2.  Chame [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) novamente e especifique [**SELFLAG \_ REMOVESELECTION**](selflag.md) no objeto restante.

 

 




