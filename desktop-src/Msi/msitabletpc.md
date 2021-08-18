---
description: o instalador definirá a propriedade MsiTabletPC como um valor diferente de zero se o sistema operacional atual for Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriedade MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac47dd0d8db3c0e882a965685bb1507dc0103f3e965dfbcb8f4857ada19e17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145600"
---
# <a name="msitabletpc-property"></a>Propriedade MsiTabletPC

o instalador definirá a propriedade **MsiTabletPC** como um valor diferente de zero se o sistema operacional atual for Windows XP Tablet PC Edition. O instalador usa a função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com o **SM \_ Tablet** e a propriedade recebe o valor diferente de zero retornado por essa função. se o sistema atual não for Windows XP Tablet PC Edition, a função **GetSystemMetrics** retornará zero e o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 4,5 no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
