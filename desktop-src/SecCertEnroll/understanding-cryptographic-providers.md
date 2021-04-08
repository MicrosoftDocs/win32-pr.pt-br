---
description: Os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários. Os provedores podem ser implementados em hardware, software ou ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Noções básicas sobre provedores criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922291"
---
# <a name="understanding-cryptographic-providers"></a>Noções básicas sobre provedores criptográficos

O conceito do provedor criptográfico que foi introduzido na Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e que evoluiu um pouco na [*Cryptography API:*](/windows/desktop/SecGloss/c-gly) a CNG (próxima geração) é fundamental para a implementação segura da funcionalidade criptográfica nos sistemas operacionais da Microsoft. Esses dois SDKs foram usados para criar vários aplicativos e são chamados internamente por outros SDKs. Por exemplo, Active Directory serviços de certificados e a API de registro de certificado dependem de CryptoAPI e CNG.

Em geral, os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários. Os provedores podem ser implementados em hardware, software ou ambos. Os aplicativos criados com o uso de CryptoAPI ou CNG não podem alterar as chaves criadas pelos provedores e não podem alterar a implementação do algoritmo criptográfico. Os vários provedores criados pela Microsoft são distribuídos com os sistemas operacionais. Outros provedores foram criados e distribuídos por terceiros.

Os tópicos a seguir destacam as diferenças entre os provedores associados ao CryptoAPI e os associados à CNG. Normalmente, esta documentação se refere a provedores sem referência ao SDK com o qual eles estão associados, observando a associação somente quando ela é relevante.

-   [Provedores de serviço de criptografia CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Provedores de algoritmos criptográficos CNG](cng-cryptographic-algorithm-providers.md)
-   [Provedores de armazenamento de chaves CNG](cng-key-storage-providers.md)
-   [Enumerando provedores instalados](enumerating-installed-providers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de registro de certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
