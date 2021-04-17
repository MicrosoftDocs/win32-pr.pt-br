---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceAvailable como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriedade PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747955"
---
# <a name="primaryvolumespaceavailable-property"></a>Propriedade PrimaryVolumeSpaceAvailable

O instalador define o valor da propriedade **PrimaryVolumeSpaceAvailable** como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) .

## <a name="remarks"></a>Comentários

Por exemplo, se [**PrimaryVolumePath**](primaryvolumepath.md) for definido como "D:" e o volume D: tiver 446.134.272 bytes livres, **PrimaryVolumeSpaceAvailable** será definido como 871356.

Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




