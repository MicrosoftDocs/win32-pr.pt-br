---
description: O instalador define a propriedade System64Folder como o caminho completo para a pasta System64 predefinida. A propriedade System64Folder existente é definida como a pasta correspondente de 32 bits.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriedade System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d586451ab596f5b480c74f382659596128a12c041596dec3c530b18307af2820
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500426"
---
# <a name="system64folder-property"></a>Propriedade System64Folder

O instalador define a propriedade **System64Folder** como o caminho completo para a pasta System64 predefinida. A propriedade **System64Folder** existente é definida como a pasta correspondente de 32 bits.

## <a name="remarks"></a>Comentários

O instalador define essa propriedade no Windows de 64 bits. por exemplo, no Windows de 64 bits, o valor pode ser C: \\ Window \\ System32. Essa propriedade não é usada em Windows de 32 bits.

essa pasta normalmente é um subdiretório da pasta Windows. No entanto, ele reside em um servidor quando configurado para Windows compartilhado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




