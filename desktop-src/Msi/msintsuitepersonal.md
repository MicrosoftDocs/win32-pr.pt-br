---
description: no Windows xp e em sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuitePersonal como 1 se o sistema operacional for Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propriedade MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c946b707e0d66a2c5bd3cd9cb6bf75828be9dd8f21e0e81080910a9fac73d353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944485"
---
# <a name="msintsuitepersonal-property"></a>Propriedade MsiNTSuitePersonal

no Windows xp e em sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuitePersonal** como 1 se o sistema operacional for Windows XP Home Edition. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador pessoal do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
