---
description: Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador. Os assemblies compartilhados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662592"
---
# <a name="shared-assemblies"></a>Assemblies compartilhados

Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador. Os assemblies compartilhados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.

Os assemblies compartilhados são instalados como [assemblies lado a lado](side-by-side-assemblies.md). O Windows Installer instala assemblies compartilhados lado a lado na pasta WinSxS. Os assemblies não são registrados globalmente no sistema, mas estão globalmente disponíveis para qualquer aplicativo que especifique uma dependência no assembly em um arquivo de manifesto. Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

Em sistemas operacionais anteriores ao Windows XP, os assemblies compartilhados geralmente são instalados na pasta do sistema do Windows e registrados globalmente. A versão mais recente instalada está disponível para qualquer aplicativo associado a ele.

Para obter informações sobre como criar um pacote de Windows Installer para instalar um assembly compartilhado, consulte o seguinte:

-   [Instalando assemblies do Win32 para compartilhamento lado a lado no Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
