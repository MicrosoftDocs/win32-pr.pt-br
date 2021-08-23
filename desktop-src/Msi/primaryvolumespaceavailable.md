---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceAvailable como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriedade PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9336bfa32ebb3bf0c12b7e7fc54ddad2b26cd635c820ca6e8ea2caabe163ceb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580666"
---
# <a name="primaryvolumespaceavailable-property"></a>Propriedade PrimaryVolumeSpaceAvailable

O instalador define o valor da propriedade **PrimaryVolumeSpaceAvailable** como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade [**PrimaryVolumePath.**](primaryvolumepath.md)

## <a name="remarks"></a>Comentários

Por exemplo, se [**PrimaryVolumePath**](primaryvolumepath.md) for definido como "D:" e o volume D: tiver 446.134.272 bytes livres, **PrimaryVolumeSpaceAvailable** será definido como 871356.

Observe que se esse valor deve ser exibido em um controle de Texto estático [,](text-control.md)o bit [FormatSize](formatsize-control-attribute.md) pode ser usado para formatar e rotular automaticamente esse número em unidades de quilobytes ou megabytes, conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




