---
description: Componentes de SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componentes de SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010591"
---
# <a name="sid-components"></a>Componentes de SID

Um valor de SID inclui componentes que fornecem informações sobre a estrutura e os componentes de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid) que identificam exclusivamente um confiável. Um SID consiste nos seguintes componentes:

-   O nível de revisão da estrutura de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid)
-   Um valor de autoridade de identificador de 48 bits que identifica a autoridade que emitiu o SID
-   Um número variável de subautoridade ou valores de RID ( [*identificador relativo*](/windows/desktop/SecGloss/r-gly) ) que identificam exclusivamente o Trustee relativo à autoridade que emitiu o Sid

A combinação do valor de autoridade de identificador e os valores de subautoridade garante que nenhum Sid seja o mesmo, mesmo que duas autoridades de emissão de SID diferentes emitam a mesma combinação de valores de RID. Cada autoridade emissora de SID emite um determinado RID apenas uma vez.

Os SIDs são armazenados em formato binário em uma estrutura de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid) . Para exibir um SID, você pode chamar a função [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) para converter um SID binário em formato de cadeia de caracteres. Para converter uma cadeia de caracteres de SID de volta para um SID válido e funcional, chame a função [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .

Essas funções usam a seguinte notação de cadeia de caracteres padronizada para SIDs, o que torna mais simples Visualizar seus componentes:

s-*R* - *I* - *s*...

Nessa notação, o caractere literal "S" identifica a série de dígitos como um SID, *R* é o nível de revisão, *I* é o valor da autoridade de identificação e *S*... é um ou mais valores de subautoridade.

O exemplo a seguir usa essa notação para exibir o SID relativo do domínio conhecido do grupo local de administradores:

S-1-5-32-544

Neste exemplo, o SID tem os seguintes componentes. As constantes entre parênteses são uma autoridade de identificador bem conhecida e valores de [*RID*](/windows/desktop/SecGloss/r-gly) definidos em Winnt. h:

-   Um nível de revisão de 1
-   Um valor de autoridade de identificação de 5 ( \_ autoridade de segurança NT \_ )
-   Um primeiro valor de subautoridade de 32 (segurança \_ interna do \_ RID do domínio \_ )
-   Um segundo valor de subautoridade de 544 ( \_ Administradores RID de alias de domínio \_ \_ )

 

 
