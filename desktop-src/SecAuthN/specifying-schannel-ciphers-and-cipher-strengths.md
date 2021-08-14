---
description: Especificando codificações schannel e pontos fortes de codificação
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Especificando codificações schannel e pontos fortes de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ef036038c3c0f759bdf4f2c2d18f0ac005ac01563d2779c5fcac02999fe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917272"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Especificando codificações schannel e pontos fortes de codificação

Para trocas de informações de cliente/servidor, o comportamento padrão do Schannel é negociar a melhor codificação disponível com base nas habilitadas no Registro. Os aplicativos podem limitar as codificações e os pontos fortes de codificação permitidos para uma conexão usando membros da estrutura [**\_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) da seguinte forma:

1.  De definir **o membro palgSupportedAlgs** como uma matriz de [**\_ ID alg**](../seccrypto/alg-id.md) que contém as codificações que permitem. Para obter mais informações, consulte IDs de criptografia.
2.  De definir os membros **dwMinimumCipherStrength** e/ou **dwMaximumCipherStrength** como os pontos fortes mínimo e máximo permitidas. Para obter mais informações, consulte Valores de força de criptografia.
3.  Passe a [**estrutura \_ CRED SCHANNEL**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por meio do parâmetro *pAuthData)* em uma chamada para a [**função AcquireCredentialsHandle.**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) Essa função retorna um handle de credenciais.
4.  Especifique o handle de credenciais em uma chamada para a função [**InitializeSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) do lado do cliente ou a função [**AcceptSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) do lado do servidor.

## <a name="cipher-ids"></a>IDs de criptografia

O comportamento padrão do Schannel é solicitar a melhor codificação disponível com base em entradas Schannel no registro do sistema. Não altere o registro do sistema; as configurações que ele contém para o Schannel são usadas globalmente e afetarão outros aplicativos. Para ver a lista de constantes válidas, consulte [**\_ ID do ALG.**](../seccrypto/alg-id.md)

## <a name="cipher-strength-values"></a>Valores de força de criptografia

Esse recurso Schannel normalmente é usado para limitar uma conexão a codificações de força de exportação ou nacionais. Os pontos fortes internos incluem 56 e 128 bits, enquanto a força da exportação é limitada a 56 bits. Se você definir os valores mínimo e máximo como zero, o Schannel usará todos os pontos fortes de criptografia disponíveis.

Usando TLS ou SSL 3.0, defina o membro **dwMinimumCipherStrength** como -1 (um negativo) para habilitar os suites de criptografia "Criptografia Nula", que fornecem assinaturas, mas nenhuma criptografia. Se **dwMaximumCipherStrength** também estiver definido como -1, somente os suites de "Criptografia Nula" serão habilitados. Essa configuração destina-se apenas ao desenvolvimento e não deve ser usada em sistemas de produção.

## <a name="querying-cipher-information"></a>Consultando informações de criptografia

Para recuperar as configurações de força de criptografia de uma credencial, chame a função [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) e especifique SECPKG ATTR CIPHER STRENGTHS como o \_ \_ parâmetro \_ *ulAttribute.*

Para recuperar a lista de algoritmos com suporte para uma credencial, chame [**o QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) com SECPKG ATTR SUPPORTED ALGS como o \_ parâmetro \_ \_ *ulAttribute.*

 

 
