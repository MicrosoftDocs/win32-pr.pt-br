---
description: A propriedade PreferredSubpictureStream recupera o fluxo de subimagem preferencial para a sessão de exibição atual.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propriedade PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825766"
---
# <a name="preferredsubpicturestream-property"></a>Propriedade PreferredSubpictureStream

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `PreferredSubpictureStream` propriedade recupera o fluxo de subimagem preferencial para a sessão de exibição atual.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o fluxo de subimagem preferencial atual no registro do sistema.

## <a name="remarks"></a>Comentários

O fluxo de subimagem preferencial é definido com [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)do objeto [MSDVDAdm](msdvdadm-object.md) .

 

 



