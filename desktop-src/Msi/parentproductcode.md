---
description: Durante uma instalação simultânea, o instalador define a propriedade ParentProductCode na sessão da instalação simultânea com o mesmo valor que a propriedade ProductCode na sessão da instalação pai.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Propriedade ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748147"
---
# <a name="parentproductcode-property"></a>Propriedade ParentProductCode

Durante uma instalação simultânea, o instalador define a propriedade **ParentProductCode** na sessão da instalação simultânea com o mesmo valor que a propriedade [**ProductCode**](productcode.md) na sessão da instalação pai. As instalações pai executam as ações de instalação simultânea para executar uma instalação simultânea. Um pacote de instalação pode determinar se ele está sendo instalado por uma ação de instalação simultânea verificando o valor dessa propriedade.

> [!Note]  
> As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).

 

> [!Note]  
> Essa propriedade não será definida se a instalação simultânea estiver sendo executada pela ação [RemoveExistingProducts](removeexistingproducts-action.md) .

 

## <a name="remarks"></a>Comentários

Para impedir que um pacote nunca seja instalado como uma instalação simultânea, adicione uma das instruções condicionais a seguir à tabela [LaunchCondition](launchcondition-table.md) . Isso impede que o pacote nunca seja instalado por uma ação de instalação simultânea executada por outra instalação. Isso não impede que o pacote seja instalado pela ação [RemoveExistingProducts](removeexistingproducts-action.md) .

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




