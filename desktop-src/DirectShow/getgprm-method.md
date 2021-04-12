---
description: O método GetGPRM recupera o registro de parâmetro geral especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Método GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500615"
---
# <a name="getgprm-method"></a>Método GetGPRM

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetGPRM` método recupera o registro de parâmetro geral especificado.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica o registro a ser recuperado como um inteiro. O valor deve variar de 0 a 15.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o registro especificado.

## <a name="remarks"></a>Comentários

Esse método não é necessário para qualquer funcionalidade de navegação ou reprodução de DVD usando o objeto **MSWebDVD** . Ele é fornecido para aqueles com uma compreensão completa da especificação de DVD que desejam implementar recursos avançados. GPRMs pode ser usado para armazenar quaisquer valores, para que possam ser configurados e lidos livremente. Mas como GPRMs também são usadas para armazenar comandos de disco, alterar seus valores usando [**SetGPRM**](setgprm-method.md) pode resultar em um comportamento imprevisível.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



