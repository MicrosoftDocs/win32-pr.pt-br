---
description: O método DVDAdm.GetParentalCountry recupera o país/região dos pais que foi salvo pela última vez no Registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeeee55a3e39449c48e1af6b2674db85d5c4a964e730e5a66bb91be6dca2c393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756756"
---
# <a name="getparentalcountry-method"></a>Método GetParentalCountry

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método recupera o país/região dos pais que foi salvo pela última `DVDAdm.GetParentalCountry` vez no Registro.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valor Retornado

Retorna um Inteiro que indica o código de país/região padrão armazenado no Registro.

## <a name="remarks"></a>Comentários

O país/região dos pais que esse método recupera não é necessariamente o mesmo país/região atualmente armazenado no objeto MSWebDVD.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




