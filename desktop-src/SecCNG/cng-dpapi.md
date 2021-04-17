---
description: A Microsoft introduziu a DPAPI (interface de programação de aplicativo de proteção de dados) no Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755060"
---
# <a name="cng-dpapi"></a>DPAPI CNG

A Microsoft introduziu a DPAPI (interface de programação de aplicativo de proteção de dados) no Windows 2000. A API consiste em duas funções, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata). A DPAPI faz parte do CryptoAPI e foi destinada a desenvolvedores que sabiam muito pouco sobre o uso de criptografia. As duas funções podem ser usadas para criptografar e descriptografar dados estáticos em um único computador.

A computação em nuvem, no entanto, geralmente requer que o conteúdo criptografado em um computador seja descriptografado em outro. Portanto, começando com o Windows 8, a Microsoft ampliou a ideia de usar uma API relativamente simples para abranger cenários de nuvem. Essa nova API, chamada de DPAPI-NG, permite que você compartilhe com segurança segredos (chaves, senhas, material da chave) e mensagens, protegendo-os a um conjunto de entidades que podem ser usadas para desprotegê-los em computadores diferentes após autenticação e autorização adequadas. Atualmente, há suporte para as seguintes entidades:

-   Um grupo em uma floresta Active Directory.
-   Credenciais da Web.

Para mais informações, consulte os seguintes tópicos:

-   [Provedores de proteção](protection-providers.md)
-   [Descritores de proteção](protection-descriptors.md)
-   [Formato de dados protegidos](protected-data-format.md)

O DPAPI-NG é criado com base na CNG (Cryptography Next Generation) e inclui as seguintes funções:

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
