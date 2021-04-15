---
description: O instalador definirá a propriedade OutOfDiskSpace como TRUE se qualquer volume que for um destino da instalação atual não tiver espaço em disco suficiente para acomodar a instalação.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propriedade OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760835"
---
# <a name="outofdiskspace-property"></a>Propriedade OutOfDiskSpace

O instalador definirá a propriedade **OutOfDiskSpace** como true se qualquer volume que for um destino da instalação atual não tiver espaço em disco suficiente para acomodar a instalação. Se todos os volumes tiverem espaço suficiente, o valor será FALSE. As ações de resolução de seleção usam esse valor para cancelar uma instalação e gerar uma caixa de diálogo.

Essa propriedade é válida a qualquer momento após a execução da [ação CostFinalize](costfinalize-action.md) . O status da propriedade [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) é atualizado dinamicamente sempre que o custo total da instalação é recalculado (por exemplo, sempre que o estado da instalação de qualquer recurso é alterado por meio da caixa de diálogo de [seleção](selection-dialog.md) ).

## <a name="remarks"></a>Comentários

Qualquer caixa de diálogo que dependa da propriedade **OutOfDiskSpace** para determinar se uma caixa de diálogo deve ser exibida, defina o [bit do estilo da caixa](trackdiskspace-dialog-style-bit.md) de diálogo TrackDiskSpace para que a caixa de diálogo atualize dinamicamente o espaço nos volumes de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




