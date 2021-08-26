---
description: O método ShowCursor torna o cursor visível quando o objeto MSWebDVD está no modo de tela inteira.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Método ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3013392a5dcea2b3c4c9af8ee94d54c540814b5f4221563429ee7c837dcdddd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050516"
---
# <a name="showcursor-method"></a>Método ShowCursor

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `ShowCursor` método torna o cursor visível quando o objeto **MSWebDVD** está no modo de tela inteira.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*Bshow*
</dt> <dd>

Especifica se o cursor deve ser show como um booliana.



| Valor | Descrição            |
|-------|------------------------|
| true  | Exibir o cursor        |
| false | Não mostrar o cursor |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando a exibição de DVD entra no modo de tela inteira, o cursor desaparece dentro de 3 a 5 segundos. Use esse método para tornar o cursor visível novamente se os botões de controle do aplicativo estão visíveis no modo de tela inteira.

 

 



