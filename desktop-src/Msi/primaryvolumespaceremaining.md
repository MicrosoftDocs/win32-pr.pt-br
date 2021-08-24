---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRemaining como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade PrimaryVolumePath, se todos os recursos selecionados no momento foram instalados.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propriedade PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580486"
---
# <a name="primaryvolumespaceremaining-property"></a>Propriedade PrimaryVolumeSpaceRemaining

O instalador define o valor da propriedade **PrimaryVolumeSpaceRemaining** como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade [**PrimaryVolumePath,**](primaryvolumepath.md) se todos os recursos selecionados no momento foram instalados. Assim como com [**a propriedade PrimaryVolumeSpaceAvailable,**](primaryvolumespaceavailable.md) esse número é expresso em unidades de 512 bytes.

## <a name="remarks"></a>Comentários

Observe que se esse valor deve ser exibido em um controle de Texto estático [,](text-control.md)o bit [FormatSize](formatsize-control-attribute.md) pode ser usado para formatar e rotular automaticamente esse número em unidades de quilobytes ou megabytes, conforme apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




