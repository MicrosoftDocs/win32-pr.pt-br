---
description: A propriedade CurrentSubpictureStream define ou recupera o fluxo de subtípico atual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propriedade CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821941"
---
# <a name="currentsubpicturestream-property"></a>Propriedade CurrentSubpictureStream

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentSubpictureStream` propriedade define ou recupera o fluxo de subtípico atual.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o fluxo.

## <a name="remarks"></a>Comentários

Os valores possíveis dessa propriedade são:



| Valor   | Descrição              |
|---------|--------------------------|
| 0 a 31 | O fluxo de subtípico    |
| 63      | Fluxo de taxa de bits baixa em mudo |



 

Essa propriedade é de leitura/gravação sem valor padrão. Antes de definir um novo fluxo de subpicture, chame [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para verificar se o fluxo está disponível.

Definir essa propriedade faz com que a [**propriedade SubpictureOn**](subpictureon-property.md) alterne para **True.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



