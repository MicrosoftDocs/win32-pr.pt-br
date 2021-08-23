---
description: em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteEnterprise como 1 se Windows servidor do 2000 Advanced estiver instalado.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Propriedade MsiNTSuiteEnterprise
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242bf1c95db7d4101362a7b72b4cfa99009a93cc2fa399d1b4b81d93aabbd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944649"
---
# <a name="msintsuiteenterprise-property"></a>Propriedade MsiNTSuiteEnterprise

em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteEnterprise** como 1 se Windows servidor do 2000 Advanced estiver instalado. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de Enterprise do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
