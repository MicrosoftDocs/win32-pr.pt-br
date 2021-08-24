---
description: O instalador define a propriedade RollbackDisabled quando a reposição foi desabilitada.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propriedade RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df5b392a69a04811853a449106858445969fed3b2c0598266ff3f8a1bcb51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039866"
---
# <a name="rollbackdisabled-property"></a>Propriedade RollbackDisabled

O instalador define a **propriedade RollbackDisabled** quando a reposição foi desabilitada. **RollbackDisabled** é usado por autores de pacote que precisam garantir que o instalador não desabilitou a reposição. A **propriedade RollbackDisabled** pode ser usada em uma expressão condicional que se recusa efetivamente a continuar com a instalação se a propriedade **RollbackDisabled** estiver definida.

## <a name="default-value"></a>Valor padrão

Por padrão, a reação está habilitada.

## <a name="remarks"></a>Comentários

Como [a reação](rollback-custom-actions.md) [e](commit-custom-actions.md) a confirmação não são executados enquanto a reação está desabilitada, o instalador não pode instalar corretamente um pacote que usa esses tipos de ações personalizadas em uma transação durante a instalação. Nesse caso, o autor do pacote deve incluir uma condição usando DisableRollback que impede que a instalação continue se a reação estiver desabilitada.

O valor da política DisableRollback pode ser definido por um administrador como parte da atribuição da política do sistema. Os administradores são aconselhados a não desabilitar a reação, a menos que seja necessário. Para obter mais informações sobre o valor da política DisableRollback, consulte [System Policy](system-policy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Instalação de reação](rollback-installation.md)
</dt> <dt>

[Política do sistema](system-policy.md)
</dt> <dt>

[ações personalizadas de reação](rollback-custom-actions.md)
</dt> <dt>

[fazer commit de ações personalizadas](commit-custom-actions.md)
</dt> </dl>

 

 




