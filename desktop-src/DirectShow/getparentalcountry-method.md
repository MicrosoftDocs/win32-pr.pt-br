---
description: O método DVDAdm. GetParentalCountry recupera o país/região pai que foi salvo pela última vez no registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748180"
---
# <a name="getparentalcountry-method"></a>Método GetParentalCountry

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.GetParentalCountry` método recupera o país/região pai que foi salvo pela última vez no registro.

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro que indica o código de país/região padrão armazenado no registro.

## <a name="remarks"></a>Comentários

O país/região pai que esse método recupera não é necessariamente o mesmo país/região atualmente armazenado no objeto MSWebDVD.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




