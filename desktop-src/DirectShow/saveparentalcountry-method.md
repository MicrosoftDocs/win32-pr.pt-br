---
description: O método DVDAdm. SaveParentalCountry salva o novo país/região pai do aplicativo no registro.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Método SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5391982129c799e6a565da362837a557765cf46604653f4f702ed38dcb910e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651206"
---
# <a name="saveparentalcountry-method"></a>Método SaveParentalCountry

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `DVDAdm.SaveParentalCountry` método salva o novo país/região pai do aplicativo no registro.

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Especifica o país/região pai como um inteiro.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o nome de usuário como uma cadeia de caracteres. (Ignorado no momento.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a senha como uma cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse método permite que um usuário que conhece a senha atual salve uma nova configuração de país/região pai no registro. Assim como acontece com todos os métodos de **MSDVDAdm**, esse método não afeta o nível atual no Player; Ele altera apenas a configuração do registro, de modo que, na próxima vez que o objeto MSWebDVD for criado, ele será aberto com o novo país/região. Para alterar o país/região pai no Player, chame [**SelectParentalCountry**](selectparentalcountry-method.md), que não altera a configuração do registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SaveParentalLevel**](saveparentallevel-method.md)
</dt> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




