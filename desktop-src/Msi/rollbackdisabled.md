---
description: O instalador define a propriedade RollbackDisabled quando a reversão foi desabilitada.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propriedade RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751839"
---
# <a name="rollbackdisabled-property"></a>Propriedade RollbackDisabled

O instalador define a propriedade **RollbackDisabled** quando a reversão foi desabilitada. O **RollbackDisabled** é usado por autores de pacotes que precisam garantir que o instalador não tenha desabilitado a reversão. A propriedade **RollbackDisabled** pode ser usada em uma expressão condicional que se recuse efetivamente a continuar com a instalação se a propriedade **RollbackDisabled** estiver definida.

## <a name="default-value"></a>Valor padrão

Por padrão, a reversão está habilitada.

## <a name="remarks"></a>Comentários

Como a [reversão](rollback-custom-actions.md) e a [confirmação](commit-custom-actions.md) não são executadas enquanto a reversão está desabilitada, o instalador não pode instalar corretamente um pacote que usa esses tipos de ações personalizadas em uma transação durante a instalação. Nesse caso, o autor do pacote deve incluir uma condição usando DisableRollback que impedirá a instalação de continuar se a reversão estiver desabilitada.

O valor da política DisableRollback pode ser definido por um administrador como parte da atribuição da política do sistema. Os administradores são aconselhados a não desabilitar a reversão, a menos que necessário. Para obter mais informações sobre o valor da política DisableRollback, consulte [política do sistema](system-policy.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Reverter instalação](rollback-installation.md)
</dt> <dt>

[Política do sistema](system-policy.md)
</dt> <dt>

[reverter ações personalizadas](rollback-custom-actions.md)
</dt> <dt>

[confirmar ações personalizadas](commit-custom-actions.md)
</dt> </dl>

 

 




