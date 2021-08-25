---
description: Durante uma instalação simultânea, o instalador define a propriedade ParentOriginalDatabase na sessão da instalação simultânea com o mesmo valor que a propriedade OriginalDatabase na sessão da instalação pai.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Propriedade ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31d022aa4ec7274d464943d8b3ec059ce11142f06e0e09c22bbb42ec40a2e5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913266"
---
# <a name="parentoriginaldatabase-property"></a>Propriedade ParentOriginalDatabase

Durante uma instalação simultânea, o instalador define a propriedade **ParentOriginalDatabase** na sessão da instalação simultânea com o mesmo valor que a propriedade [**OriginalDatabase**](originaldatabase.md) na sessão da instalação pai. As instalações pai usam as ações de instalação simultânea para executar uma instalação simultânea. Um pacote de instalação pode determinar se ele está sendo instalado por uma ação de instalação simultânea verificando o valor dessa propriedade.

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
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[**ParentProductCode**](parentproductcode.md)
</dt> </dl>

 

 




