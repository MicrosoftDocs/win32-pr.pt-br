---
description: O método GetGPRM recupera o registro de parâmetro geral especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Método GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c46307f1cbec49b4916cdbd528c2b22cfb42bf89a06285c5c779339786599d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812556"
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

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Especifica o registro a ser recuperado como um Inteiro. O valor deve variar de 0 a 15.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o registro especificado.

## <a name="remarks"></a>Comentários

Esse método não é necessário para nenhuma funcionalidade de navegação ou reprodução de DVD usando o **objeto MSWebDVD.** Ele é fornecido para aqueles com uma compreensão completa da especificação de DVD que deseja implementar recursos avançados. Os GPRMs podem ser usados para manter quaisquer valores, de modo que possam ser definidos e lidos livremente. Mas como os GPRMs também são usados para armazenar comandos de disco, alterar seus valores usando [**SetGPRM**](setgprm-method.md) pode resultar em comportamento imprevisível.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



