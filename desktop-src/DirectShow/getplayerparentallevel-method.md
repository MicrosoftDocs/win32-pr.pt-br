---
description: O GetPlayerParentalLevel recupera o conjunto de nível de gerenciamento de pais no objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Método GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087265"
---
# <a name="getplayerparentallevel-method"></a>Método GetPlayerParentalLevel

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetPlayerParentalLevel` recupera o nível de gerenciamento do pai definido no objeto **MSWebDVD** .

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro especificando o nível pai atual no navegador de DVD ou-1 se o gerenciamento de pais está desabilitado.

## <a name="remarks"></a>Comentários

Um aplicativo de Player é responsável por impor controles dos pais. O nível do pai do Player é um valor definido por um aplicativo do que pode ser usado para indicar o nível mais alto de pais que o usuário atual pode exibir. Quando o navegador de DVD encontra um novo nível de pai, use esse método para determinar se o novo nível é maior do que o nível definido pelo aplicativo por meio de [**SelectParentalLevel**](selectparentallevel-method.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



