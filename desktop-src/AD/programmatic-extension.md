---
title: Extensão programática
description: As extensões programáticas têm vários méritos, no entanto, um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extensão programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc8f049eb243dea0bfb8ad1eef4754d3713b9e908a16837abb832bab829b7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025464"
---
# <a name="programmatic-extension"></a>Extensão programática

O benefício de um arquivo LDIF é que o administrador pode examinar sua função. No entanto, o esquema também pode ser estendido programaticamente. As extensões programáticas têm vários méritos, mas um aplicativo é opaco; o administrador deve confiar na documentação incluída no aplicativo de instalação. O uso de extensões de esquema programático pode ser uma barreira para a implantação de aplicativos que os usam. Uma extensão programática é invariável; é um Windows NT executável. O binário não pode ser adulterado, ao contrário de um arquivo LDIF ou .csv, que pode ser editado inadvertidamente ou maliciosamente.

Os benefícios de um arquivo LDIF incluem:

-   Os aplicativos podem detectar e se recuperar de erros e fornecer comentários do usuário.
-   Os aplicativos podem manipular o Unicode sem recorrer à codificação Base64.
-   os aplicativos podem aproveitar Windows Installer APIs de instalação.
-   Os aplicativos podem ser assinados para estabelecer a autenticidade.

 

 




