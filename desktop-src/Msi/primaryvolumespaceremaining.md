---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRemaining como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade PrimaryVolumePath, se todos os recursos selecionados no momento forem instalados.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propriedade PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752841"
---
# <a name="primaryvolumespaceremaining-property"></a>Propriedade PrimaryVolumeSpaceRemaining

O instalador define o valor da propriedade **PrimaryVolumeSpaceRemaining** como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) , se todos os recursos selecionados no momento forem instalados. Assim como acontece com a propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , esse número é expresso em unidades de 512 bytes.

## <a name="remarks"></a>Comentários

Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




