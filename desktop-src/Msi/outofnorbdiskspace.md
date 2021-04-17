---
description: O instalador definirá a propriedade OutOfNoRbDiskSpace como true se qualquer volume que for um destino da instalação não tiver espaço em disco suficiente para acomodar a instalação.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propriedade OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748763"
---
# <a name="outofnorbdiskspace-property"></a>Propriedade OutOfNoRbDiskSpace

O instalador definirá a propriedade **OutOfNoRbDiskSpace** como true se qualquer volume que for um destino da instalação não tiver espaço em disco suficiente para acomodar a instalação. Nesse caso, a propriedade **OutOfNoRbDiskSpace** é definida como true mesmo que a reversão tenha sido desabilitada. Se todos os volumes tiverem espaço suficiente, o valor será false.

Um desenvolvedor de um pacote de instalação pode lidar com a situação em que a propriedade [**OutOfDiskSpace**](outofdiskspace.md) é verdadeira e a propriedade **OutOfNoRbDiskSpace** é false, criando uma interface do usuário que apresenta ao usuário uma opção para desabilitar a reversão e continuar a instalação. Para obter informações sobre como exibir condicionalmente uma caixa de diálogo, consulte [visão geral do ControlEvent,](controlevent-overview.md). Para obter informações sobre como desabilitar a reversão, consulte [EnableRollback ControlEvent,](enablerollback-controlevent.md).

A propriedade **OutOfNoRbDiskSpace** é válida a qualquer momento após a execução da [ação CostFinalize](costfinalize-action.md) . O status da propriedade **OutOfNoRbDiskSpace** é atualizado dinamicamente sempre que o custo total da instalação é recalculado (por exemplo, sempre que o estado da instalação de qualquer recurso é alterado por meio da [caixa de diálogo de seleção](selection-dialog.md)). As ações de resolução de seleção usam esse valor para cancelar uma instalação e gerar uma caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Visão geral do ControlEvent,](controlevent-overview.md)
</dt> <dt>

[**Propriedade OutOfDiskSpace**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent,](enablerollback-controlevent.md)
</dt> <dt>

[Ação CostFinalize](costfinalize-action.md)
</dt> <dt>

[Caixa de diálogo de seleção](selection-dialog.md)
</dt> </dl>

 

 




