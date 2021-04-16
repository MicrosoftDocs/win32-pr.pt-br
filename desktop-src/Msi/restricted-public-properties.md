---
description: Em determinados casos, um usuário que não é um administrador do sistema só pode substituir uma lista aprovada de propriedades públicas Windows Installerdas restritas.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Propriedades públicas restritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747525"
---
# <a name="restricted-public-properties"></a>Propriedades públicas restritas

No caso de uma instalação gerenciada, o autor do pacote pode precisar limitar quais [Propriedades públicas](public-properties.md) são passadas para o lado do servidor e podem ser alteradas por um usuário que não seja um administrador do sistema. Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios elevados. Se todas as condições a seguir forem atendidas, um usuário que não seja um administrador do sistema só poderá substituir uma lista aprovada de propriedades públicas restritas:

-   O sistema é o Windows 2000.
-   O usuário não é um administrador do sistema.
-   O aplicativo ou produto está sendo instalado com privilégios elevados.

Se todas as condições acima forem verdadeiras, o instalador usa como padrão a seguinte lista de propriedades públicas restritas que podem ser alteradas por qualquer usuário:

-   [**ACTION**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEmode**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**Nocompanyname**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**DISTRIBUÍDO**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**Inicialize**](reboot.md)
-   [**Install**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**Volte**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**TRANSFORMAÇÕES**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

O autor de um pacote de instalação pode estender essa lista padrão para incluir propriedades públicas adicionais usando a propriedade [**SecureCustomProperties**](securecustomproperties.md) .

Definir a propriedade [**EnableUserControl**](-enableusercontrol.md) ou a [política do sistema](system-policy.md) [EnableUserControl](enableusercontrol.md)estende a lista para todas as propriedades públicas. Todos os usuários podem então alterar qualquer propriedade pública.

O instalador define a propriedade [**RestrictedUserControl**](restrictedusercontrol.md) sempre que a lista de propriedades públicas passadas para o servidor por usuários não administradores é restrita.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> </dl>

 

 



