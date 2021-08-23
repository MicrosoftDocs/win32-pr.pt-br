---
description: O instalador define essa propriedade se o usuário tiver privilégios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propriedade AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b765aa4ece1bc19b5ed59e97a98ca4579042d52d65c0024ae018c794f9aaa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581906"
---
# <a name="adminuser-property"></a>Propriedade AdminUser

O instalador define essa propriedade se o usuário tiver privilégios de administrador.

**Windows Server 2008 e Windows Vista:** A **propriedade AdminUser** é a mesma que a [**propriedade Privileged.**](privileged.md) Os autores devem usar a **propriedade Privileged.** O instalador definirá essas propriedades se o usuário tiver privilégios de administrador, se o aplicativo tiver sido atribuído por um administrador do sistema ou se as políticas do usuário e do computador AlwaysInstallElevated estão definidas como true.

## <a name="remarks"></a>Comentários

As diferenças entre essas propriedades podem ter sido usadas em alguns pacotes herdados. Por exemplo, **AdminUser** pode ter sido usado em vez de [**Privileged**](privileged.md) em instruções condicionais, porque o instalador só define a propriedade **AdminUser** se o usuário for um administrador. O instalador define a **propriedade Privileged** se o usuário for um administrador ou se a política permitir que o usuário instale com privilégios elevados.

**Windows Server 2008 e Windows Vista:** Sem suporte. Privileged [](privileged.md) e **AdminUser** são os mesmos. Pacotes que exigem propriedades **Privileged** e **AdminUser** distintas podem restaurar a diferença definindo a [**propriedade MSIUSEREALADMINDETECTION.**](msiuserealadmindetection.md)

Para obter mais informações, [consulte Instalando um pacote](installing-a-package-with-elevated-privileges-for-a-non-admin.md)com privilégios elevados para uma propriedade não admin e [**Privileged.**](privileged.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Vista ou Windows Server 2008. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




