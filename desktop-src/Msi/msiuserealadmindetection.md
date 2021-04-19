---
description: Defina a propriedade MSIUSEREALADMINDETECTION como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propriedade MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768725"
---
# <a name="msiuserealadmindetection-property"></a>Propriedade MSIUSEREALADMINDETECTION

Defina a propriedade **MSIUSEREALADMINDETECTION** como 1 para solicitar que o instalador Use informações reais do usuário ao definir a propriedade [**AdminUser**](adminuser.md) . Ao executar no Windows Vista, o [**Privileged**](privileged.md) e o **AdminUser** são os mesmos. Os autores devem ter usado a propriedade **privilegiada** em novos pacotes. Pacotes herdados que exigem Propriedades distintas **privilegiadas** e **AdminUser** podem restaurar a diferença definindo a propriedade **MSIUSEREALADMINDETECTION** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,1 e versões anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




