---
description: O instalador define a propriedade System64Folder como o caminho completo para a pasta System64 predefinida. A propriedade System64Folder existente é definida como a pasta correspondente de 32 bits.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriedade System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750214"
---
# <a name="system64folder-property"></a>Propriedade System64Folder

O instalador define a propriedade **System64Folder** como o caminho completo para a pasta System64 predefinida. A propriedade **System64Folder** existente é definida como a pasta correspondente de 32 bits.

## <a name="remarks"></a>Comentários

O instalador define essa propriedade no Windows de 64 bits. Por exemplo, no Windows de 64 bits, o valor pode ser C: \\ Window \\ System32. Essa propriedade não é usada em janelas de 32 bits.

Essa pasta normalmente é um subdiretório da pasta do Windows. No entanto, ele reside em um servidor quando configurado para janelas compartilhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




