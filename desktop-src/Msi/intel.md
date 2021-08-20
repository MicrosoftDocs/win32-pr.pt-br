---
description: a propriedade Intel é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Propriedade Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5b4fe488867a67da1f97ce4564bb8ce530b89417554a91a8734bee6e863f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013234"
---
# <a name="intel-property"></a>Propriedade Intel

a propriedade **Intel** é definida pelo Windows Installer para o nível numérico do processador quando executado em um processador Intel. Os valores são os mesmos do campo *wProcessorLevel* da estrutura de [**\_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) . durante a execução em um processador x64, o Windows Installer define a propriedade **Intel** para refletir o processador x86 emulado pelo computador x64 conforme relatado pelo sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
