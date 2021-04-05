---
description: O método IsSubpictureStreamEnabled recupera um valor que indica se o fluxo de subimagem especificado está habilitado no título atual.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Método IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825942"
---
# <a name="issubpicturestreamenabled-method"></a>Método IsSubpictureStreamEnabled

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `IsSubpictureStreamEnabled` método recupera um valor que indica se o fluxo de subimagem especificado está habilitado no título atual.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o fluxo de subimagem como um inteiro.



| Valor   | Descrição              |
|---------|--------------------------|
| 0 a 31 | fluxo de subimagem        |
| 63      | fluxo de baixa taxa de bits sem áudio |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor booliano que indica se o fluxo de áudio especificado está disponível no título atual. Verdadeiro significa que está disponível.

## <a name="remarks"></a>Comentários

Embora um disco possa conter até 32 fluxos de subimagem, cada fluxo não está necessariamente disponível para cada título. Sempre verifique se um fluxo está disponível para um título antes de definir a propriedade [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .

 

 



