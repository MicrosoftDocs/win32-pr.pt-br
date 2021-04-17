---
description: A propriedade Intel é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propriedade Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782789"
---
# <a name="intel-property"></a>Propriedade Intel

A propriedade **Intel** é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel. Os valores são os mesmos do campo *wProcessorLevel* da estrutura de [**\_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) . Durante a execução em um processador x64, o Windows Installer define a propriedade **Intel** para refletir o processador x86 emulado pelo computador x64 conforme relatado pelo sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
