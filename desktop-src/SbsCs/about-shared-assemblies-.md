---
description: Um assembly compartilhado é um assembly disponível para uso por vários aplicativos no computador.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Sobre assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749973"
---
# <a name="about-shared-assemblies"></a>Sobre assemblies compartilhados

Um assembly compartilhado é um assembly disponível para uso por vários aplicativos no computador. No Windows Vista e no Windows XP, [assemblies lado a lado](about-side-by-side-assemblies-.md) podem ser instalados como assemblies compartilhados. Os assemblies compartilhados lado a lado não são registrados globalmente no sistema, mas estão globalmente disponíveis para aplicativos que especificam uma dependência no assembly em [manifestos](manifests.md). Várias versões de assemblies lado a lado podem ser compartilhadas por diferentes aplicativos em execução ao mesmo tempo. Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](about-isolated-applications-and-side-by-side-assemblies.md). Por exemplo, os [assemblies lado a lado da Microsoft com suporte](supported-microsoft-side-by-side-assemblies.md) fornecidos com o Windows XP normalmente são usados como assemblies compartilhados por vários aplicativos.

Os assemblies compartilhados lado a lado são instalados na pasta WinSxS. Publicadores de assembly, aplicativos e administradores podem alterar a versão das dependências de assembly lado a lado após a implantação por meio da [configuração](configuration.md). Os assemblies compartilhados lado a lado podem ser instalados por uma atualização do sistema operacional ou por um pacote Windows Installer que instala ou atualiza um aplicativo. Para obter mais informações, consulte [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).

Antes do Windows XP, os assemblies compartilhados eram registrados globalmente e instalados na pasta System do Windows. Nesse caso, a versão mais recente instalada do assembly está disponível para qualquer aplicativo que se vincule a ele. Um assembly lado a lado também pode ser instalado como um assembly privado para o uso exclusivo de um aplicativo. Para obter mais informações, consulte [assemblies privados](/windows/desktop/Msi/private-assemblies).

 

 
