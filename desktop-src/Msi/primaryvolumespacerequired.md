---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRequired como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propriedade PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c644c53b5a36c8ba834a52c22ca3ba2b192499cbf351f122d8ed2b6a66a57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042256"
---
# <a name="primaryvolumespacerequired-property"></a>Propriedade PrimaryVolumeSpaceRequired

O instalador define o valor da propriedade **PrimaryVolumeSpaceRequired** como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) . Assim como acontece com a propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , esse número é expresso em unidades de 512 bytes.

## <a name="remarks"></a>Comentários

Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows instalador 4,0 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




