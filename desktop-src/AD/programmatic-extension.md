---
title: Extensão programática
description: As extensões programáticas têm vários méritos, no entanto, um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extensão programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634929"
---
# <a name="programmatic-extension"></a>Extensão programática

O benefício de um arquivo LDIF é que o administrador pode examinar sua função. No entanto, o esquema também pode ser estendido programaticamente. As extensões programáticas têm vários méritos, mas um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação. O uso de extensões de esquema programático pode ser uma barreira para a implantação de aplicativos que os usam. Uma extensão programática é invariável; é um executável do Windows NT. O binário não pode ser adulterado, ao contrário de um arquivo LDIF ou. csv, que pode ser editado inadvertidamente ou maliciosamente.

Os benefícios de um arquivo LDIF incluem:

-   Os aplicativos podem detectar e se recuperar de erros e fornecer comentários do usuário.
-   Os aplicativos podem manipular o Unicode sem recorrer à codificação Base64.
-   Os aplicativos podem aproveitar Windows Installer APIs de instalação.
-   Os aplicativos podem ser assinados para estabelecer a autenticidade.

 

 




