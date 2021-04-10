---
description: Codificação e decodificação de um contexto de certificado usando o CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codificando e decodificando um contexto de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164823"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codificando e decodificando um contexto de certificado

O [*CryptoAPI*](../secgloss/c-gly.md) dá suporte à codificação e decodificação de [*certificados*](../secgloss/c-gly.md). O CryptoAPI inclui um sistema abrangente e flexível de funções e estruturas C que permitem codificação e decodificação de várias maneiras. O CryptoAPI dá suporte à estrutura de certificado [*X. 509*](../secgloss/x-gly.md) padrão e à codificação de [*notação de sintaxe abstrata*](../secgloss/a-gly.md) padrão (ASN. 1) para fornecer interoperabilidade com outros sistemas.

Para obter uma visão geral dos dados codificados, consulte [dados codificados e decodificados](encoded-and-decoded-data.md).

## <a name="certificate-contexts"></a>Contextos de certificado

Um [*contexto de certificado*](../secgloss/c-gly.md), o [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)do certificado, é uma estrutura C que contém um membro codificado, um identificador para um [*repositório de certificados*](../secgloss/c-gly.md), um ponteiro para o blob de [*certificado*](../secgloss/c-gly.md)codificado original e um ponteiro para uma estrutura de [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) C.

A estrutura de [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) é o coração do certificado. Ele contém, em forma direta e em formato codificado, todas as informações básicas no certificado. A ilustração a seguir mostra a estrutura de **\_ informações de certificado** com todos os seus membros codificados mostrados como sombreados.

![estrutura de informações de certificado \-](images/certinf2.png)

Os membros **IssuerUniqueID** e **SubjectUniqueID** fazem parte da implementação do certificado [*X. 509*](../secgloss/x-gly.md) versão 2, mas raramente são usados. As extensões de certificado na versão 3 substituem a funcionalidade desses membros.

Se as informações contidas no **emissor** de membros codificados (sombreados) e o **assunto** forem necessários, esses membros deverão ser decodificados. Use [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) para decodificar esses membros. A ilustração a seguir mostra o processo de decodificação de um desses membros.

![decodificando com CryptDecodeObject](images/infoflow.png)

No caso ilustrado, a função [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) cria uma estrutura de [**\_ \_ informações de nome de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) , uma matriz de estruturas [**\_ RDN de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , uma matriz correspondente de estruturas [**\_ \_ attr de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) e uma cadeia de caracteres que contém o nome. Os membros da **estrutura \_ \_ attr do RDN de certificado** determinam o conteúdo da cadeia de caracteres. Por exemplo, se o membro **pszObjId** for 2.5.4.3, a cadeia de caracteres conterá um nome comum. Se for 2.5.4.10, a cadeia de caracteres conterá um nome de organização. Para obter uma lista desses [*identificadores de objeto*](../secgloss/o-gly.md) (OIDs), **consulte \_ \_ atributo RDN de certificado**.

O membro **dwValueType** contém informações sobre o tipo de cadeia de caracteres. Se ela for \_ \_ uma cadeia de caracteres imprimível do RDN de certificado \_ , o membro de valor conterá uma cadeia de caracteres de largura de byte, terminada em zero. Se for um certificado \_ de \_ \_ cadeia de caracteres Unicode RDN, a cadeia de caracteres será uma cadeia de caracteres de largura dupla (tamanho do Word).

Para obter um processo detalhado de codificação e decodificação de certificados, consulte [codificando uma \_ estrutura de informações de certificado](encoding-a-cert-info-structure.md) e [decodificando uma \_ estrutura de informações de certificado](decoding-a-cert-info-structure.md).

 

 
