---
description: O GetPlayerParentalLevel recupera o nível de gerenciamento dos pais definido no objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Método GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0426c48589449e03b78d894300ff2c83d83d625a269b19f0e985f78d49973f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756476"
---
# <a name="getplayerparentallevel-method"></a>Método GetPlayerParentalLevel

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetPlayerParentalLevel` recupera o nível de gerenciamento dos pais definido no objeto **MSWebDVD.**

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro especificando o nível dos pais atual no Navegador de DVD ou -1 se o gerenciamento dos pais estiver desabilitado.

## <a name="remarks"></a>Comentários

Um aplicativo de player é responsável por impor controles dos pais. O nível dos pais do jogador é um valor definido por um aplicativo que pode ser usado para indicar o nível mais alto dos pais que o usuário atual pode exibir. Quando o Navegador de DVD encontrar um novo nível dos pais, use esse método para determinar se o novo nível é maior que o nível definido pelo aplicativo por meio de [**SelectParentalLevel.**](selectparentallevel-method.md)

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

 

 



