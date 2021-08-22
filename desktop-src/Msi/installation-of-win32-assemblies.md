---
description: Instale assemblies Win32 tornando-os um componente do pacote do Microsoft Windows Installer que instala ou atualiza seu aplicativo.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalação de assemblies Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c680d53e1c4702bab3b9a24920b18a2fdb644a86c41207712ec3726a310a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633836"
---
# <a name="installation-of-win32-assemblies"></a>Instalação de assemblies Win32

Instale assemblies Win32 tornando-os um componente do pacote do Microsoft Windows Installer que instala ou atualiza seu aplicativo. Quando você autora a tabela [MsiAssembly](msiassembly-table.md) e a [tabela MsiAssemblyName](msiassemblyname-table.md), isso identifica o componente na coluna Componente \_ como um assembly. O instalador definirá a propriedade [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) como a versão de arquivo do Sxs.dll em sistemas operacionais que podem dar suporte a assemblies Win32 e não definir essa propriedade de outra forma.

No Windows Vista e Windows XP, Windows Instalador não escreve informações de assembly no Registro. Além disso, assemblies compartilhados, assemblies privados e assemblies lado a lado podem ser usados. Para obter informações, [consulte Assemblies compartilhados,](shared-assemblies.md) [assemblies privados](private-assemblies.md)e [assemblies lado a lado.](side-by-side-assemblies.md)

As seções a seguir descrevem como autor de um pacote do Windows Installer para instalar assemblies Win32 como compartilhados, privados ou lado a lado em diferentes Windows operacionais.

-   [Instalando assemblies win32 para compartilhamento lado a lado no Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalando assemblies Win32 para o uso privado de um aplicativo no Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



