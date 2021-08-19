---
description: O CAPICOM usa certificados digitais para criar assinaturas, criptografar chaves de criptografia de sessão ao criar mensagens enveloadas e descriptografar chaves de sessão criptografadas quando uma mensagem envelografada é recebida.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Usando armazenamentos de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f687286d40e64e590079d872a0134742d552b66a9926a1febeb5c42ae2ad7566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971608"
---
# <a name="using-certificate-stores"></a>Usando armazenamentos de certificados

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

O CAPICOM usa [*certificados*](../secgloss/d-gly.md) digitais para criar assinaturas, criptografar chaves de criptografia de sessão ao criar mensagens enveloadas e descriptografar chaves de sessão criptografadas quando uma mensagem envelografada é recebida. Por padrão, CAPICOM usa certificados no Meu armazenamento que têm uma chave privada associada para criação de [*assinaturas*](../secgloss/d-gly.md) digitais e descriptografia de chave de sessão. Na maioria dos casos, um aplicativo nunca precisaria abrir ou lidar diretamente com um armazenamento de certificados.

No entanto, os aplicativos que criam mensagens enveloadas usam [*a chave pública*](../secgloss/p-gly.md) de cada destinatário pretendido de uma mensagem enveloada. Essas chaves são recuperadas dos certificados dos destinatários pretendido. Portanto, para criar mensagens enveloadas para um grupo de destinatários pretendido, os certificados desses destinatários seriam coletados em um armazenamento de certificados.

A tabela a seguir lista os armazenamentos de certificados padrão normalmente persistentes em uma estação de usuário.



| Repositório        | Descrição                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Meu           | Contém certificados pessoais. Esses certificados geralmente terão uma chave privada associada.                                                                                                                                                                                                                                                                             |
| Outras pessoas | Contém os certificados daqueles dos que o usuário normalmente envia mensagens enveloadas ou recebe mensagens assinadas.                                                                                                                                                                                                                                                     |
| Ca e Root  | Contém os [*certificados de*](../secgloss/r-gly.md) autoridades de certificação em que o usuário confia para emitir certificados para outras pessoas. Os certificados nesses armazenamentos normalmente são fornecidos com o sistema operacional ou pelo administrador de rede do usuário. Os certificados no armazenamento raiz normalmente são auto-assinados. |



 

Os armazenamentos de USUÁRIO ATUAIS CAPICOM adicionais podem ser criados, abertos e \_ \_ persistentes, dando um nome de loja diferente como uma cadeia de caracteres. Se um armazenamento com esse nome não existir, um armazenamento vazio será criado e aberto. Se um armazenamento existir, ele será aberto e todos os certificados atualmente no armazenamento serão disponibilizados.

As seções a seguir mostram exemplos para tarefas de armazenamento de certificados:

-   [Abrindo o Armazenamento do Active Directory e recuperando certificados](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Adicionando certificados a um armazenamento de certificados](adding-certificates-to-a-certificate-store.md)
-   [Usando lojas em locais diferentes](using-stores-in-different-locations.md)
-   [Coletando e verificando certificados](collecting-and-verifying-certificates.md)

 

 
