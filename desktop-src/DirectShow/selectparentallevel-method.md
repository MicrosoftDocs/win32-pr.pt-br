---
description: O método SelectParentalLevel define o nível de pai especificado para reprodução subsequente.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Método SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684036"
---
# <a name="selectparentallevel-method"></a>Método SelectParentalLevel

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `SelectParentalLevel` método define o nível de pai especificado para reprodução subsequente.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica o nível de gerenciamento do pai como um inteiro. Para habilitar o gerenciamento de pais, o parâmetro *iLevel* deve variar de 1 a 8. Para desabilitar o gerenciamento de pais, defina *iLevel* como-1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica o usuário atual como uma cadeia de caracteres. (Ignorado no momento.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica a senha atualmente armazenada no registro como uma cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse método define o nível de acesso no objeto MSWebDVD, que determina qual conteúdo o usuário pode reproduzir. Níveis mais altos podem reproduzir conteúdo de nível inferior, mas níveis inferiores não podem reproduzir conteúdo de nível superior. O significado exato dos oito níveis de gerenciamento de pais de DVD varia dependendo do país/região. No Estados Unidos e no Canadá, os níveis são mapeados para as categorias de classificação da MPAA (Associação de imagem de movimento da América). O gerenciamento de pais no navegador de DVD está desabilitado por padrão.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
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

 

 



