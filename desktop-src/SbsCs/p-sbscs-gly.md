---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370570"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (aplicativos isolados e assemblies lado a lado)

[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuração por aplicativo**
</dt> <dd>

Configuração que pode substituir a configuração de aplicativo global de um assembly específico. Uma configuração por aplicativo é especificada por um arquivo de manifesto de configuração de aplicativo instalado na mesma pasta que o arquivo executável. O arquivo de manifesto descreve a versão, ou o intervalo de versões, de assemblies lado a lado a serem usados pelo aplicativo. A configuração por aplicativo pode ser usada quando uma nova versão de um assembly é incompatível com um aplicativo. Nesse caso, a configuração padrão ou global do aplicativo pode ser substituída por um assembly lado a lado específico.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**assembly lado a lado privado**
</dt> <dd>

Um assembly lado a lado privado só é visível para um aplicativo especificado. Ele é instalado localmente em um aplicativo isolado e o código do assembly se torna privado para o contexto do aplicativo. As dependências de um assembly lado a lado privado são descritas no arquivo de manifesto do aplicativo. Assemblies privados lado a lado podem ser usados para deslocar os efeitos negativos do compartilhamento de assembly, como conflitos de DLL e para facilitar a implantação do aplicativo.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token de chave pública**
</dt> <dd>

Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado. A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais. Necessário para todos os assemblies compartilhados lado a lado.

</dd> </dl>

 

 



