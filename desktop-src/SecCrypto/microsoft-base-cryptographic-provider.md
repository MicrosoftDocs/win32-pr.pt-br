---
description: O provedor Microsoft Base Cryptographic é o provedor de CSP (provedor de serviços de criptografia) inicial e é distribuído com as versões 1,0 e 2,0 do CryptoAPI. É um provedor de uso geral que dá suporte a assinaturas digitais e criptografia de dados.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provedor criptográfico base da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32082fc6cd7ec6d34bd994e3d3122e2b4c06eee290af8074cea0c183e5dd0116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100696"
---
# <a name="microsoft-base-cryptographic-provider"></a>Provedor criptográfico base da Microsoft

O provedor Microsoft Base Cryptographic é o provedor de CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) inicial e é distribuído com as versões 1,0 e 2,0 do [*CryptoAPI*](../secgloss/c-gly.md) . É um provedor de uso geral que dá suporte a [*assinaturas digitais*](../secgloss/d-gly.md) e criptografia de dados.

O algoritmo de chave pública RSA é usado para todas as operações de chave pública.

Para manter a compatibilidade com versões anteriores, a nova versão do provedor retém a designação da versão 1,0 do nome em Wincrypt. h. No entanto, a versão 2,0 deste provedor está sendo fornecida no momento. Para determinar a versão real do provedor em uso, chame [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com o argumento *DwParam* definido como **PP \_ version**. Se 0x0200 for retornado em *pbData*, você terá a versão 2,0.

|                   | Valor            |
|-------------------|------------------|
| **Tipo de provedor** | PROV \_ RSA \_ completo  |
| **Nome do provedor** | Prov de MS \_ Def \_    |



 

 

 
