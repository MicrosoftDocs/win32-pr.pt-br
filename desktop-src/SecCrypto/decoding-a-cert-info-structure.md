---
description: Dado um certificado, a primeira etapa na decodificação do BLOB de certificado é chamar CertCreateCertificateContext, passando um ponteiro para o certificado codificado (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decodificando uma estrutura de CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8eab5a75c2a5906ac875f925845f83f3c411c12a31aeea4825efd795b78eaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100868"
---
# <a name="decoding-a-cert_info-structure"></a>Decodificando uma \_ estrutura de informações de certificado

Dado um certificado, a primeira etapa na decodificação do [*blob*](../secgloss/b-gly.md) de certificado é chamar [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), passando um ponteiro para o certificado codificado (*blob*). Quando essa função é chamada, ela cria uma duplicata do certificado codificado, cria uma estrutura do tipo [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)e cria uma estrutura do tipo [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Conforme mostrado na ilustração a seguir, um [*contexto de certificado*](../secgloss/c-gly.md) inclui o *blob* de certificado original, uma estrutura c do tipo **\_ contexto** de certificado e uma estrutura c do tipo **\_ informações de certificado**. Um dos membros da estrutura de **\_ contexto de certificado** aponta para a estrutura de **\_ informações de certificado** e outro para o blob de certificado codificado.

![contexto do certificado](images/certcntx.png)

O objeto codificado (membro de dados) sempre é fornecido como a entrada para a função [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) , e a saída é uma estrutura C que pode ou não ter membros codificados, dependendo do seu processo.

Há um outro membro que requer alguma decodificação, que é o membro de **extensão** . Embora não esteja codificado no nível de [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , ele contém algumas informações codificadas. Para decodificar essas informações, prossiga conforme mostrado na ilustração a seguir.

![decodificando informações](images/xtension.png)

Na estrutura [**de \_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , o membro **rgExtension** é um ponteiro para uma matriz de estruturas de [**\_ extensão de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) . Cada estrutura de **\_ extensão de certificado** tem um membro de **valor** que está na forma codificada e precisa ser decodificada. O membro de **valor** é passado para a função [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) e, em seguida, a saída da função depende do valor do membro **pszObjId** . Observe que, na ilustração, duas estruturas diferentes são produzidas, uma das [**\_ informações de \_ restrições \_ básicas de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) de tipo e uma das informações de ID de chave de autoridade de certificação de tipo, dependendo do valor de **pszObjId**. [**\_ \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info)

 

 
