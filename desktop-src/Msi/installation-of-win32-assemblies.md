---
description: Instale os assemblies do Win32 tornando-os um componente do pacote Microsoft Windows Installer que instala ou atualiza seu aplicativo.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalação de assemblies Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749796"
---
# <a name="installation-of-win32-assemblies"></a>Instalação de assemblies Win32

Instale os assemblies do Win32 tornando-os um componente do pacote Microsoft Windows Installer que instala ou atualiza seu aplicativo. Quando você cria a [tabela MsiAssembly](msiassembly-table.md) e a [tabela MsiAssemblyName](msiassemblyname-table.md), isso identifica o componente na \_ coluna componente como um assembly. O instalador definirá a propriedade [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) para a versão de arquivo do Sxs.dll em sistemas operacionais que podem dar suporte a assemblies Win32 e não definir essa propriedade de outra forma.

No Windows Vista e no Windows XP, Windows Installer não grava informações de assembly no registro. Além disso, assemblies compartilhados, assemblies privados e assemblies lado a lado podem ser usados. Para obter informações, consulte [assemblies compartilhados](shared-assemblies.md), [assemblies privados](private-assemblies.md)e [assemblies lado a lado](side-by-side-assemblies.md).

As seções a seguir descrevem como criar um pacote de Windows Installer para instalar assemblies do Win32 como compartilhado, privado ou lado a lado em sistemas operacionais Windows diferentes.

-   [Instalando assemblies do Win32 para compartilhamento lado a lado no Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



