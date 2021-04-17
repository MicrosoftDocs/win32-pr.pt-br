---
description: A propriedade WindowlessActivation Inicializa o objeto MSWebDVD no tempo de design para o modo de janela ou sem janela.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propriedade WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770243"
---
# <a name="windowlessactivation-property"></a>Propriedade WindowlessActivation

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `WindowlessActivation` Propriedade Inicializa o objeto **MSWebDVD** no tempo de design para o modo de janela ou sem janela.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Valor Retornado

Retorna se o objeto está no modo de janela como um booliano.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de true. Portanto, você só precisa definir essa propriedade se estiver executando o objeto **MSWebDVD** em um contêiner em janela. Quando contido em uma página da Web no Microsoft® Internet Explorer, o **MSWebDVD** está sempre no modo sem janela e você não precisa definir essa propriedade.

 

 



