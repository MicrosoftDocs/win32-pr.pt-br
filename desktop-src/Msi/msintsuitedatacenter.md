---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador define a propriedade MsiNTSuiteDataCenter como 1 se Windows 2000 Datacenter Server estiver instalado.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propriedade MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b42edc0a4abb544133b4b7fb176988f826c5af172cc4c0d49ca56494ed37672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082806"
---
# <a name="msintsuitedatacenter-property"></a>Propriedade MsiNTSuiteDataCenter

No Windows 2000 e sistemas operacionais posteriores, o instalador define a propriedade **MsiNTSuiteDataCenter** como 1 se Windows 2000 Datacenter Server estiver instalado. O instalador define essa propriedade como 1 somente se o sinalizador VER \_ SUITE \_ DATACENTER estiver definido na [**estrutura OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
