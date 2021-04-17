---
description: O instalador definirá a propriedade MsiTabletPC como um valor diferente de zero se o sistema operacional atual for o Windows XP Tablet PC Edition.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Propriedade MsiTabletPC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754354"
---
# <a name="msitabletpc-property"></a>Propriedade MsiTabletPC

O instalador definirá a propriedade **MsiTabletPC** como um valor diferente de zero se o sistema operacional atual for o Windows XP Tablet PC Edition. O instalador usa a função [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com o **SM \_ Tablet** e a propriedade recebe o valor diferente de zero retornado por essa função. Se o sistema atual não for o Windows XP Tablet PC Edition, a função **GetSystemMetrics** retornará zero e o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 4,5 no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
