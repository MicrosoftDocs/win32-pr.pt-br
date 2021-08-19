---
description: em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteBackOffice como 1 se os componentes do Microsoft backoffice estiverem instalados.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Propriedade MsiNTSuiteBackOffice
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf3c65e1f5d1d528dd35232900a9aef12bdf344d1d2859eef814d1030e6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944821"
---
# <a name="msintsuitebackoffice-property"></a>Propriedade MsiNTSuiteBackOffice

em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteBackOffice** como 1 se os componentes do Microsoft backoffice estiverem instalados. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador do BackOffice do ver Suite \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
