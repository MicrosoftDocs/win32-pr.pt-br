---
description: Um assembly compartilhado é um assembly disponível para uso por vários aplicativos no computador.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Sobre assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5db7f10ea5ffa6e04fd5cd905262eb026b4ca4c24309ffd4c53cb10f9df00b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142619"
---
# <a name="about-shared-assemblies"></a>Sobre assemblies compartilhados

Um assembly compartilhado é um assembly disponível para uso por vários aplicativos no computador. No Windows Vista e Windows XP, [assemblies](about-side-by-side-assemblies-.md) lado a lado podem ser instalados como assemblies compartilhados. Assemblies compartilhados lado a lado não são registrados globalmente no sistema, mas estão disponíveis globalmente para aplicativos que especificam uma dependência no assembly nos [manifestos](manifests.md). Várias versões de assemblies lado a lado podem ser compartilhadas por diferentes aplicativos em execução ao mesmo tempo. Para obter mais informações, consulte [Sobre aplicativos isolados e assemblies lado a lado.](about-isolated-applications-and-side-by-side-assemblies.md) Por exemplo, os [assemblies](supported-microsoft-side-by-side-assemblies.md) lado a lado da Microsoft com suporte fornecidos com o Windows XP normalmente são usados como assemblies compartilhados por vários aplicativos.

Assemblies compartilhados lado a lado são instalados na pasta WinSxS. Editores de assembly, aplicativos e administradores podem alterar a versão das dependências de assembly lado a lado após a implantação por meio da [configuração](configuration.md). Assemblies compartilhados lado a lado podem ser instalados por uma atualização do sistema operacional ou por um pacote do instalador Windows que instala ou atualiza um aplicativo. Para obter mais informações, [consulte Instalação de assemblies Win32](../msi/installation-of-win32-assemblies.md).

Antes de Windows XP, os assemblies compartilhados eram registrados globalmente e instalados na pasta Windows System. Nesse caso, a versão instalada mais recente do assembly está disponível para qualquer aplicativo que se a vinícar a ele. Um assembly lado a lado também pode ser instalado como um assembly privado para o uso exclusivo de um aplicativo. Para obter mais informações, consulte [Assemblies privados.](/windows/desktop/Msi/private-assemblies)

 

 
