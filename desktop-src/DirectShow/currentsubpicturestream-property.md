---
description: A propriedade CurrentSubpictureStream define ou recupera o fluxo de subimagem atual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propriedade CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500679"
---
# <a name="currentsubpicturestream-property"></a>Propriedade CurrentSubpictureStream

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentSubpictureStream` propriedade define ou recupera o fluxo de subimagem atual.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o fluxo.

## <a name="remarks"></a>Comentários

Os valores possíveis dessa propriedade são:



| Valor   | Descrição              |
|---------|--------------------------|
| 0 a 31 | O fluxo de subimagem    |
| 63      | Fluxo de baixa taxa de bits sem áudio |



 

Esta propriedade é de leitura/gravação sem valor padrão. Antes de definir um novo fluxo de subimagem, chame [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para verificar se o fluxo está disponível.

Definir essa propriedade faz com que a propriedade [**subpictureize**](subpictureon-property.md) seja alternada para **true**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Subimagem**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



