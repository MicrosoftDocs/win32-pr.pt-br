---
description: A propriedade MsiNetAssemblySupport indica se o computador dá suporte a assemblies de tempo de execução de idioma comum.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propriedade MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751848"
---
# <a name="msinetassemblysupport-property"></a>Propriedade MsiNetAssemblySupport

A propriedade **MsiNetAssemblySupport** indica se o computador dá suporte a assemblies de tempo de execução de idioma comum. Em sistemas que oferecem suporte a assemblies de tempo de execução de idioma comum, o instalador define o valor de **MsiNetAssemblySupport** para a versão de arquivo de Fusion.dll. O instalador não definirá essa propriedade se o sistema operacional não oferecer suporte a assemblies de tempo de execução de idioma comum. Quando várias versões do Fusion.dll são instaladas lado a lado no computador do usuário, essa propriedade é definida como a versão mais recente do arquivo de Fusion.dll. Por exemplo, se .NET Framework versão 1.0.3705 (Fusion.dll versão 1.0.3705.15) e .NET Framework versão 1.1.4322 (Fusion.dll versão 1.1.4322.314) forem instaladas lado a lado, a propriedade **MsiNetAssemblySupport** será definida como 1.1.4322.314. Para obter mais informações, consulte [assemblies](assemblies.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




