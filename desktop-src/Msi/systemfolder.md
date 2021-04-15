---
description: O instalador define a propriedade SystemFolder como o caminho completo da pasta do sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propriedade SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760826"
---
# <a name="systemfolder-property"></a>Propriedade SystemFolder

O instalador define a propriedade **SystemFolder** como o caminho completo da pasta do sistema.

## <a name="remarks"></a>Comentários

O instalador define essa propriedade. Por exemplo, no Windows de 32 bits, o valor pode ser C: \\ Windows \\ System32. No Windows de 64 bits, o valor pode ser C: \\ Windows \\ SysWOW64.

Essa pasta normalmente é um subdiretório da pasta do Windows. No entanto, ele reside em um servidor quando configurado para janelas compartilhadas.

Essa pasta é local, mesmo quando configurada para janelas compartilhadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




