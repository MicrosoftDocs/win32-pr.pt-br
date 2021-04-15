---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteDataCenter como 1 se o Windows 2000 Datacenter Server estiver instalado.
ms.assetid: a777e62a-a360-4d8c-b7a6-00d45c17db66
title: Propriedade MsiNTSuiteDataCenter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106b9119885e15b94bf5d8f2cd4b6954d0891d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747536"
---
# <a name="msintsuitedatacenter-property"></a>Propriedade MsiNTSuiteDataCenter

No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteDataCenter** como 1 se o Windows 2000 Datacenter Server estiver instalado. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de datacenter do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
