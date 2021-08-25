---
description: Os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários. Os provedores podem ser implementados em hardware, software ou ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Noções básicas sobre provedores criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f167f186ed4da1ac5e97aba8a3c4659f13f29f253de3f489981fc6b32810015f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127216"
---
# <a name="understanding-cryptographic-providers"></a>Noções básicas sobre provedores criptográficos

O conceito de provedor criptográfico introduzido na API de Criptografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e que evoluiu um pouco na API de [*Criptografia:*](/windows/desktop/SecGloss/c-gly) CNG (Próxima Geração) é fundamental para a implementação segura da funcionalidade criptográfica em sistemas operacionais da Microsoft. Esses dois SDKs foram usados para criar muitos aplicativos e são chamados internamente por outros SDKs. Por exemplo, Serviços de Certificados do Active Directory e a API de Registro de Certificado dependem de CryptoAPI e CNG.

Em geral, os provedores implementam algoritmos criptográficos, geram chaves, fornecem armazenamento de chaves e autenticam usuários. Os provedores podem ser implementados em hardware, software ou ambos. Aplicativos criados usando CryptoAPI ou CNG não podem alterar as chaves criadas pelos provedores e não podem alterar a implementação do algoritmo criptográfico. Os vários provedores criados pela Microsoft são distribuídos com os sistemas operacionais. Outros provedores foram criados e distribuídos por terceiros.

Os tópicos a seguir realçam as diferenças entre os provedores associados ao CryptoAPI e os associados ao CNG. Normalmente, essa documentação refere-se a provedores sem referência ao SDK ao qual eles estão associados, notando a associação somente quando for relevante.

-   [Provedores de serviços criptográficos cryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Provedores de algoritmo criptográfico CNG](cng-cryptographic-algorithm-providers.md)
-   [Provedores de Armazenamento CNG](cng-key-storage-providers.md)
-   [Enumerando provedores instalados](enumerating-installed-providers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a API de Registro de Certificado](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
