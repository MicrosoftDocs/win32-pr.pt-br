---
description: A propriedade MsiNetAssemblySupport indica se o computador dá suporte a assemblies common language run-time.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propriedade MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d135fcc9eb301d3624586318fdc0d5dbbc534c5771ee89d4ae625af78b0782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944899"
---
# <a name="msinetassemblysupport-property"></a>Propriedade MsiNetAssemblySupport

A **propriedade MsiNetAssemblySupport** indica se o computador dá suporte a assemblies common language run-time. Em sistemas que suportam assemblies de common language run time, o instalador define o valor **de MsiNetAssemblySupport** como a versão do arquivo Fusion.dll. O instalador não definirá essa propriedade se o sistema operacional não dá suporte a assemblies de common language run-time. Quando várias versões do Fusion.dll são instaladas lado a lado no computador do usuário, essa propriedade é definida como a versão mais recente do arquivo Fusion.dll. Por exemplo, se .NET Framework versão 1.0.3705 (Fusion.dll versão 1.0.3705.15) e .NET Framework versão 1.1.4322 (Fusion.dll versão 1.1.4322.314) serão instalados lado a lado, A **propriedade MsiNetAssemblySupport** é definida como 1.1.4322.314. Para obter mais informações, consulte [Assemblies](assemblies.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




