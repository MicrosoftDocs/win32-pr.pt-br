---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRequired como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propriedade PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749784"
---
# <a name="primaryvolumespacerequired-property"></a>Propriedade PrimaryVolumeSpaceRequired

O instalador define o valor da propriedade **PrimaryVolumeSpaceRequired** como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) . Assim como acontece com a propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , esse número é expresso em unidades de 512 bytes.

## <a name="remarks"></a>Comentários

Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




