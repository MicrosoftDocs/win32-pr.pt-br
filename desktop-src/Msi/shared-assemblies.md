---
description: Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador. Os assemblies compartilhados devem ser instalados por um Windows instalador usado para instalar ou atualizar um aplicativo.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1097a0f2bbbc4d91a6206734cb2dead53bb38748b82c0204daff476d3eb663e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628506"
---
# <a name="shared-assemblies"></a>Assemblies compartilhados

Um assembly Win32 pode ser instalado como um assembly compartilhado e estar disponível para uso por vários aplicativos no computador. Os assemblies compartilhados devem ser instalados por um Windows instalador usado para instalar ou atualizar um aplicativo.

Assemblies compartilhados são instalados [como assemblies lado a lado.](side-by-side-assemblies.md) O Windows instalador do Windows instala assemblies compartilhados lado a lado na pasta Winsxs. Os assemblies não são registrados globalmente no sistema, mas estão disponíveis globalmente para qualquer aplicativo que especifique uma dependência no assembly em um arquivo de manifesto. Para obter mais informações, [consulte Aplicativos isolados e Assemblies lado a lado.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

Em sistemas operacionais anteriores Windows XP, assemblies compartilhados geralmente são instalados na pasta Windows sistema e registrados globalmente. A versão mais recente instalada está disponível para qualquer aplicativo que se a bind a ela.

Para obter informações sobre como Windows pacote do instalador para instalar um assembly compartilhado, consulte o seguinte:

-   [Instalando assemblies win32 para compartilhamento lado a lado no Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalando assemblies Win32 para o uso privado de um aplicativo no Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
