---
description: O método de exibição de cursor torna o cursor visível quando o objeto MSWebDVD está no modo de tela inteira.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Método de concursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825829"
---
# <a name="showcursor-method"></a>Método de concursor

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `ShowCursor` método torna o cursor visível quando o objeto **MSWebDVD** está no modo de tela inteira.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*
</dt> <dd>

Especifica se o cursor deve ser mostrado como um booliano.



| Valor | Descrição            |
|-------|------------------------|
| true  | Exibir o cursor        |
| false | Não mostrar o cursor |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Quando a exibição do DVD entra no modo de tela inteira, o cursor desaparece dentro de 3 a 5 segundos. Use esse método para tornar o cursor visível novamente se os botões de controle do seu aplicativo estiverem visíveis no modo de tela inteira.

 

 



