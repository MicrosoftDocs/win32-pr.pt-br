---
description: O instalador define a propriedade OutOfNoRbDiskSpace como True se qualquer volume que é um destino da instalação tiver espaço em disco insuficiente para acomodar a instalação.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propriedade OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275eec4c78a1fe0074fe8e91f7dcab3b660cade46eb8810aa992edf6a45fb989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942766"
---
# <a name="outofnorbdiskspace-property"></a>Propriedade OutOfNoRbDiskSpace

O instalador define a **propriedade OutOfNoRbDiskSpace** como True se qualquer volume que é um destino da instalação tiver espaço em disco insuficiente para acomodar a instalação. Nesse caso, a **propriedade OutOfNoRbDiskSpace** é definida como True mesmo se a reposição tiver sido desabilitada. Se todos os volumes têm espaço suficiente, o valor é False.

Um desenvolvedor de um pacote de instalação pode lidar com a situação quando a propriedade [**OutOfDiskSpace**](outofdiskspace.md) é True e a propriedade **OutOfNoRbDiskSpace** é False, com a composição de uma interface do usuário que apresenta ao usuário uma opção para desabilitar a replicação e continuar a instalação. Para obter informações sobre como exibir condicionalmente uma caixa de diálogo, consulte [Visão geral de ControlEvent](controlevent-overview.md). Para obter informações sobre como desabilitar a reação, consulte [EnableRollback ControlEvent](enablerollback-controlevent.md).

A **propriedade OutOfNoRbDiskSpace** é válida a qualquer momento após a execução da ação [CostFinalize.](costfinalize-action.md) O status **da propriedade OutOfNoRbDiskSpace** é atualizado dinamicamente sempre que o custo total da instalação é recalculado (por exemplo, sempre que o estado de instalação de qualquer recurso é alterado por meio da caixa de diálogo [Seleção](selection-dialog.md)). As ações de resolução de seleção usam esse valor para cancelar uma instalação e gerar uma caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Visão geral de ControlEvent](controlevent-overview.md)
</dt> <dt>

[**Propriedade OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[Ação CostFinalize](costfinalize-action.md)
</dt> <dt>

[Caixa de diálogo Seleção](selection-dialog.md)
</dt> </dl>

 

 




