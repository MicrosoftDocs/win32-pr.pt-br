---
description: Usando uma cadeia de caracteres de construtor de objeto para construir um componente
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Usando uma cadeia de caracteres de construtor de objeto para construir um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457047"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Usando uma cadeia de caracteres de construtor de objeto para construir um componente

O exemplo a seguir ilustra como recuperar e usar programaticamente uma cadeia de caracteres de construtor de objeto quando um componente é instanciado. Ele mostra uma implementação da interface [**constructodeobjetoi**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) que recupera uma cadeia de caracteres de construtor de objeto. A cadeia de caracteres pode ser analisada para definir valores iniciais ou influenciar o comportamento do componente.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de cadeias de caracteres do construtor de objeto COM+](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Especificando uma cadeia de caracteres de construtor de objeto para um componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



