---
description: Especificando codificações Schannel e níveis de codificação
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Especificando codificações Schannel e níveis de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750453"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Especificando codificações Schannel e níveis de codificação

Para trocas de informações de cliente/servidor, o comportamento padrão do Schannel é negociar a melhor codificação disponível com base nas habilitadas no registro. Os aplicativos podem limitar as codificações e os pontos de codificação permitidos para uma conexão usando membros da estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) da seguinte maneira:

1.  Defina o membro **palgSupportedAlgs** como uma matriz de [**\_ ID de alg**](../seccrypto/alg-id.md) que contém as codificações permitidas. Para obter mais informações, consulte IDs de codificação.
2.  Defina os membros **dwMinimumCipherStrength** e/ou **dwMaximumCipherStrength** para os pontos fortes mínimos e máximos permitidos. Para obter mais informações, consulte valores de intensidade de codificação.
3.  Passe a estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por meio do parâmetro *pAuthData* ) em uma chamada para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Essa função retorna um identificador de credenciais.
4.  Especifique o identificador de credenciais em uma chamada para a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) do lado do cliente ou a função [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) do lado do servidor.

## <a name="cipher-ids"></a>IDs de codificação

O comportamento padrão do Schannel é solicitar a melhor codificação disponível com base nas entradas do Schannel no registro do sistema. Não altere o registro do sistema; as configurações que ele contém para Schannel são usadas globalmente e afetarão outros aplicativos. Para obter a lista de constantes válidas, consulte [**\_ ID de alg**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Valores de intensidade de codificação

Normalmente, esse recurso Schannel é usado para limitar uma conexão a codificações de força doméstica ou de exportação. As forças domésticas incluem 56 e 128 bits, enquanto a intensidade da exportação é limitada a 56 bits. Se você definir os valores mínimo e máximo como zero, o Schannel usará todos os níveis de codificação disponíveis.

Usando TLS ou SSL 3,0, defina o membro **dwMinimumCipherStrength** como-1 (negativo) para habilitar os conjuntos de codificação de "criptografia nula", que fornecem assinaturas, mas sem criptografia. Se **dwMaximumCipherStrength** também for definido como-1, somente os pacotes de "criptografia nula" serão habilitados. Essa configuração destina-se somente ao desenvolvimento e não deve ser usada em sistemas de produção.

## <a name="querying-cipher-information"></a>Consultando informações de codificação

Para recuperar as configurações de intensidade de codificação para uma credencial, chame a função [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) e especifique os \_ pontos de codificação de attr SECPKG \_ \_ como o parâmetro *ulAttribute* .

Para recuperar a lista de algoritmos com suporte para uma credencial, chame o [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) com o SECPKG \_ attr com \_ suporte \_ ALGS como o parâmetro *ulAttribute* .

 

 
