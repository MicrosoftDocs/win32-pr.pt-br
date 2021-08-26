---
description: Defina a propriedade MSIUSEREALADMINDETECTION como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propriedade MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a177d320aff25cf21b932ca25e691f145f94ad3
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812933"
---
# <a name="msiuserealadmindetection-property"></a>Propriedade MSIUSEREALADMINDETECTION

Defina a propriedade **MSIUSEREALADMINDETECTION** como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade [**AdminUser**](adminuser.md) . ao executar o Windows Vista, os [**privilégios**](privileged.md) e **AdminUser** são os mesmos. Os autores devem usar a propriedade **Privileged** em novos pacotes. Pacotes herdados que exigem Propriedades distintas **privilegiadas** e **AdminUser** podem restaurar a diferença definindo a propriedade **MSIUSEREALADMINDETECTION** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




