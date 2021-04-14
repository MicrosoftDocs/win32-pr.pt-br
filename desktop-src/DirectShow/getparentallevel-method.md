---
description: O método DVDAdm. GetParentalLevel recupera o nível pai que foi salvo pela última vez no registro.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Método GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370069"
---
# <a name="getparentallevel-method"></a>Método GetParentalLevel

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.GetParentalLevel` método recupera o nível pai que foi salvo pela última vez no registro.

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro de 1 a 8 indicando o nível pai padrão.

## <a name="remarks"></a>Comentários

O nível pai que esse método recupera não é necessariamente o mesmo nível atualmente armazenado no controle MSWebDVD; para obter o nível atualmente armazenado no controle, chame o método [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) . Um valor de-1 indica que o gerenciamento de pais está desabilitado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



