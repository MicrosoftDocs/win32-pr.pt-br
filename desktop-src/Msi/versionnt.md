---
description: O instalador define a propriedade VersionNT para o número de versão do sistema operacional, indefinido se o sistema operacional não for Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propriedade VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752435"
---
# <a name="versionnt-property"></a>Propriedade VersionNT

O instalador define a propriedade **VersionNT** para o número de versão do sistema operacional, indefinido se o sistema operacional não for Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 ou Windows 7. O valor é um inteiro: MajorVersion \* 100 + MinorVersion.

Instruções condicionais que dependem do sistema operacional podem usar essa propriedade.

Consulte também [valores de Propriedade do sistema operacional](operating-system-property-values.md).

## <a name="remarks"></a>Comentários

As expressões de condição podem testar o Windows NT, o Windows 2000 ou o Windows XP usando o nome da propriedade, ou podem verificar a versão usando um operador de comparação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




