---
description: O método AcceptParentalLevelChange aceita ou rejeita o novo nível temporário de gerenciamento de pais.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Método AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873586"
---
# <a name="acceptparentallevelchange-method"></a>Método AcceptParentalLevelChange

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método AcceptParentalLevelChange aceita ou rejeita o novo nível temporário de gerenciamento de pais.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Especifica o novo nível de pai como um valor booliano.



| Valor | Descrição                               |
|-------|-------------------------------------------|
| true  | Aceite o novo nível de gerenciamento de pais. |
| false | Rejeite o novo nível de gerenciamento de pais. |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Chame esse método em resposta a uma \_ notificação de evento de alteração de nível pai de DVD do EC \_ \_ \_ para especificar se o navegador de DVD deve reproduzir o conteúdo com o novo nível de pai ou Branch para onde o disco especifica se o novo nível é rejeitado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Impondo níveis de gerenciamento de pais](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



