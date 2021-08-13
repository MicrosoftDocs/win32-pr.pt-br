---
description: a partir do Windows 8, a Microsoft começou a distribuir os provedores que permitem compartilhar com segurança segredos e mensagens criptografados entre computadores.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Provedores de proteção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fe4c688eec734a7c32d1a85eaec2d9ebf132834a5970802cecb2639240e7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907187"
---
# <a name="protection-providers"></a>Provedores de proteção

a partir do Windows 8, a Microsoft começou a distribuir os provedores que permitem compartilhar com segurança segredos e mensagens criptografados entre computadores. Atualmente, há dois provedores de proteção de chave. O provedor de proteção de chave da Microsoft permite que você proteja o conteúdo a um grupo em uma floresta Active Directory. O provedor de proteção de chave do cliente da Microsoft permite que você proteja o conteúdo para um conjunto de credenciais da Web.

O protetor correto a ser usado é escolhido automaticamente para você quando a função [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analisa a cadeia de caracteres de regra do descritor de proteção que você fornece como entrada. O provedor de proteção de chave da Microsoft é escolhido para cadeias de caracteres de regra que começam com SID, SDDL e LOCAL. O provedor de proteção de chave do cliente da Microsoft analisa cadeias de caracteres de regra que começam com webcredentials. Para obter mais informações sobre cadeias de caracteres de regra, consulte [descritores de proteção](protection-descriptors.md).

> [!Note]  
> Os provedores personalizados não são permitidos no momento. [DPAPI CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descritores de proteção](protection-descriptors.md)
</dt> </dl>

 

 



