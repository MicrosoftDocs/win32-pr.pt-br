---
description: O método SelectParentalCountry define o país/região dos pais especificado para reprodução subsequente.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Método SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d148145f2c38cdb01da209e02f6400301da851e1d2b41e5adaf84b2338ad21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684056"
---
# <a name="selectparentalcountry-method"></a>Método SelectParentalCountry

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SelectParentalCountry` método define o país/região dos pais especificado para reprodução subsequente.

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*Icountry*
</dt> <dd>

Especifica o país/região como um Inteiro.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o usuário conectado atual como uma Cadeia de Caracteres. (Atualmente ignorado.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a cadeia de caracteres da senha do aplicativo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O país/região dos pais determina como os níveis dos pais são interpretados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



