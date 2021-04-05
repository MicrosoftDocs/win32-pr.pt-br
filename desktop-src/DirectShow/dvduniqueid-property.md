---
description: A propriedade DVDUniqueID recupera um número gerado pelo sistema que identifica exclusivamente o disco atual.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propriedade DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825792"
---
# <a name="dvduniqueid-property"></a>Propriedade DVDUniqueID

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DVDUniqueID` propriedade recupera um número gerado pelo sistema que identifica exclusivamente o disco atual.

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que identifica exclusivamente o disco atual.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. O número do identificador (ID) não é absolutamente exclusivo, mas é exclusivo para todas as finalidades práticas. A ID se aplica a todas as cópias replicadas de um disco. Em outras palavras, todas as cópias de um filme específico têm a mesma ID. A ID é baseada em tamanhos de arquivo, datas e outras informações, e não no valor BCA.

 

 



