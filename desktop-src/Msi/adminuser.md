---
description: O instalador definirá essa propriedade se o usuário tiver privilégios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propriedade AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751863"
---
# <a name="adminuser-property"></a>Propriedade AdminUser

O instalador definirá essa propriedade se o usuário tiver privilégios de administrador.

**Windows Server 2008 e Windows Vista:** A propriedade **AdminUser** é igual à propriedade [**Privileged**](privileged.md) . Os autores devem ter usado a propriedade **Privileged** . O instalador definirá essas propriedades se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador de sistema ou se as políticas de usuário e máquina AlwaysInstallElevated estiverem definidas como true.

## <a name="remarks"></a>Comentários

As diferenças entre essas propriedades podem ter sido usadas em alguns pacotes herdados. Por exemplo, **AdminUser** pode ter sido usado em vez de [**Privileged**](privileged.md) em instruções condicionais, pois o instalador só define a propriedade **AdminUser** se o usuário for um administrador. O instalador definirá a propriedade **privilegiada** se o usuário for um administrador ou se a política permitir que o usuário instale com privilégios elevados.

**Windows Server 2008 e Windows Vista:** Sem suporte. [**Privileged**](privileged.md) e **AdminUser** são os mesmos. Os pacotes que exigem Propriedades distintas **privilegiadas** e **AdminUser** podem restaurar a diferença definindo a propriedade [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .

Para obter mais informações, consulte [instalando um pacote com privilégios elevados para uma propriedade não administrativa](installing-a-package-with-elevated-privileges-for-a-non-admin.md)e [**privilegiada**](privileged.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Vista ou no Windows Server 2008. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




