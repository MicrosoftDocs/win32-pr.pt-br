---
description: A CNG tem os seguintes recursos.
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: Recursos da CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434c72075c04b0c280c85831ca78d930c0fcc047de19609d11764bcf63ddad56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908443"
---
# <a name="cng-features"></a>Recursos da CNG

A CNG tem os seguintes recursos.

-   [Agilidade criptográfica](#cryptographic-agility)
-   [Certificação e conformidade](#certification-and-compliance)
-   [Suporte a Suite B](#suite-b-support)
-   [Suporte herdado](#legacy-support)
-   [Suporte ao modo kernel](#kernel-mode-support)
-   [Auditoria](#auditing)
-   [Geradores de números aleatórios substituíveis](#replaceable-random-number-generators)
-   [Acesso thread-safe](#thread-safety)
-   [Modo de operação](#mode-of-operation)

## <a name="cryptographic-agility"></a>Agilidade criptográfica

Uma das principais proposições de valor da CNG é a agilidade criptográfica, às vezes chamada de independente de criptografia. No entanto, a conversão de implementação de protocolos como [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL) ou TLS (segurança de [*camada de transporte*](/windows/desktop/SecGloss/t-gly) ), CMS (S/MIME), IPsec, Kerberos e assim por diante, foi necessária para tornar essa capacidade valiosa. No nível da CNG, era necessário fornecer substituição e descoberta para todos os tipos de algoritmos (funções simétricas, assimétricas, de hash), geração de números aleatórios e outras funções de utilitário. As alterações no nível de protocolo são mais significativas porque, em muitos casos, as APIs de protocolo precisavam adicionar a seleção de algoritmos e outras opções de flexibilidade que não existiam anteriormente.

a CNG está disponível primeiro no Windows Vista e está posicionada para substituir os usos existentes de [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) em toda a pilha de software da Microsoft. Os desenvolvedores de terceiros encontrarão muitos recursos novos na CNG, incluindo:

-   Um novo sistema de configuração de criptografia, dando suporte à melhor agilidade de criptografia.
-   Abstração mais refinada para armazenamento de chaves (e separação de armazenamento de operações de algoritmos).
-   Isolamento de processo para operações com chaves de longo prazo.
-   Geradores de números aleatórios substituíveis.
-   Alívio da exportação de restrições de assinatura.
-   Segurança de thread em toda a pilha.
-   API criptográfica do modo kernel.

Além disso, a CNG inclui suporte para todos os algoritmos de Suite B necessários, incluindo o ECC ( [*criptografia de curva elíptica*](/windows/desktop/SecGloss/e-gly) ). Os aplicativos CryptoAPI existentes continuarão funcionando conforme a CNG se tornar disponível.

## <a name="certification-and-compliance"></a>Certificação e conformidade

a CNG é validada para o FIPS 140-2 (Federal Information Processing standards) e faz parte do destino da avaliação para a Windows certificação de critérios comuns. A CNG foi projetada para ser utilizável como um componente em um sistema validado pelo FIPS nível 2.

A CNG está em conformidade com os requisitos de critérios comuns por meio do armazenamento e uso de chaves de vida longa em um processo seguro.

## <a name="suite-b-support"></a>Suporte a Suite B

Um recurso importante da CNG é seu suporte para os algoritmos de Suite B. Em fevereiro de 2005, a NSA (Agência de segurança nacional) do Estados Unidos anunciou um conjunto coordenado de criptografia simétrica, contrato de segredo simétrico (também conhecido como troca de chaves), assinatura digital e funções de hash para uso futuro do governo dos EUA chamados *Suite B*. A NSA anunciou que as implementações de Suite B certificadas podem e serão usadas para proteção de informações designadas como principais segredos, segredos e informações privadas que, no passado, foram descritas como confidenciais, mas não classificadas. Por isso, Suite B suporte é muito importante para fornecedores de software de aplicativo e integradores de sistema, bem como para a Microsoft.

Todos os algoritmos de Suite B são conhecidos publicamente. Eles foram desenvolvidos fora do escopo do sigilo governamental historicamente associado ao desenvolvimento de algoritmos criptográficos. Nesse mesmo período de tempo, alguns países e regiões europeus também propuseram os mesmos requisitos de Suite B para proteger suas informações.

a criptografia de Suite B recomenda o uso de Diffie-Hellman de curva elíptica (ECDH) em muitos protocolos existentes, como o protocolo IKE (IKE, usado principalmente no IPsec), TLS ( [*transport layer security*](/windows/desktop/SecGloss/t-gly) ) e mime (S/mime) seguros.

A CNG inclui suporte para Suite B que se estende a todos os algoritmos necessários: AES (todos os tamanhos de chave), família SHA-2 (SHA-256, SHA-384 e SHA-512) de algoritmos de hashing, ECDH e o ECDSA (DSA de curva elíptica) nas curvas elementares padrão do NIST P-256, P-384 e P-521. as curvas binárias, as curvas Koblitz, as curvas primos personalizadas e a curva elíptica Menezes-t-Vanstone (ECMQV) não têm suporte dos provedores de algoritmos da Microsoft incluídos no Windows Vista.

## <a name="legacy-support"></a>Suporte herdado

A CNG fornece suporte para o conjunto atual de algoritmos no [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1,0. Todos os algoritmos que atualmente têm suporte no *CryptoAPI* 1,0 continuarão a ter suporte na CNG.

## <a name="kernel-mode-support"></a>Suporte ao modo kernel

A CNG dá suporte à criptografia no modo kernel. As mesmas APIs são usadas no modo kernel e de usuário para oferecer suporte total aos recursos de criptografia. O SSL/TLS e o IPsec operam no modo kernel, além dos processos de inicialização que usarão a CNG. Nem todas as funções CNG podem ser chamadas do modo kernel. O tópico de referência para as funções que não podem ser chamadas do modo kernel irá declarar explicitamente que a função não pode ser chamada do modo kernel. Caso contrário, todas as funções CNG poderão ser chamadas do modo kernel se o chamador estiver sendo executado no [*IRQL*](/windows/desktop/SecGloss/i-gly)de **\_ nível passivo** . Além disso, algumas funções CNG de modo kernel podem ser chamadas **no \_ nível de expedição IRQL**, dependendo dos recursos do provedor.

A interface do provedor de suporte do Microsoft kernel Security (Ksecdd.sys) é um módulo criptográfico baseado em software e de uso geral que reside no nível do modo kernel de Windows. Ksecdd.sys é executado como um driver de exportação de modo kernel e fornece serviços de criptografia por meio de suas interfaces documentadas para componentes de kernel. O único algoritmo de provedor da Microsoft interno que não tem suporte pelo Ksecdd.sys é DSA.

**Windows Server 2008 e Windows Vista:** A CNG não dá suporte a algoritmos e provedores conectáveis no modo kernel. Os únicos algoritmos de criptografia com suporte disponíveis no modo kernel são as implementações fornecidas pela Microsoft por meio das APIs CNG do modo kernel.

## <a name="auditing"></a>Auditoria

Para atender a alguns dos requisitos de critérios comuns, além de fornecer segurança abrangente, muitas ações que ocorrem na camada CNG são auditadas no KSP (provedor de armazenamento de chaves de software) da Microsoft. O KSP da Microsoft segue as seguintes diretrizes para criar registros de auditoria no log de segurança:

-   Falhas de geração de chave e par de chaves, incluindo falhas de teste automático, devem ser auditadas.
-   A importação e a exportação de chave devem ser auditadas.
-   As falhas de destruição de chave devem ser auditadas.
-   As chaves persistentes precisam ser auditadas quando são gravadas e lidas a partir de arquivos.
-   As falhas de verificação de consistência por pares devem ser auditadas.
-   As falhas de validação da chave secreta, se houver, devem ser auditadas, por exemplo, verificações de paridade em chaves 3DES.
-   As falhas na criptografia, na descriptografia, no hash, na assinatura, na verificação, na troca de chaves e na geração de números aleatórios devem ser auditadas.
-   Os autotestes de criptografia devem ser auditados.

Em geral, se uma chave não tiver um nome, ela será uma chave efêmera. Uma chave efêmera não persiste e o KSP da Microsoft não gera registros de auditoria para chaves efêmeras. O KSP da Microsoft gera registros de auditoria no modo de usuário somente no processo LSA. Nenhum registro de auditoria é gerado pelo CNG do modo kernel. Os administradores precisam configurar a política de auditoria para obter todos os logs de auditoria do KSP do log de segurança. Um administrador deve executar a seguinte linha de comando para configurar auditorias adicionais geradas pelo KSPs:

**Auditpol/set/SubCategory: "outros eventos do sistema"/success: habilitar/Failure: habilitar**

## <a name="replaceable-random-number-generators"></a>Geradores de números aleatórios substituíveis

Outra melhoria que a CNG fornece é a capacidade de substituir o gerador de número aleatório padrão (RNG). No CryptoAPI, é possível fornecer um RNG alternativo como parte de um CSP (provedor de serviços de criptografia), mas não é possível redirecionar os CSPs de base da Microsoft para usar outro RNG. A CNG possibilita especificar explicitamente um determinado RNG a ser usado em chamadas específicas.

## <a name="thread-safety"></a>Acesso thread-safe

Todas as funções que modificam a mesma área de memória ao mesmo tempo (seções críticas) quando são chamadas de threads separados não são thread-safe.

## <a name="mode-of-operation"></a>Modo de operação

A CNG dá suporte a cinco modos de operações que podem ser usadas com codificações de bloco simétricas por meio de APIs de criptografia. Esses modos e sua compatibilidade são listados na tabela a seguir. O modo de operação pode ser alterado definindo a propriedade [**de \_ \_ modo de encadeamento BCRYPT**](cng-property-identifiers.md) para o provedor de algoritmo usando a função [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .



| Modo de operação           | Valor do modo de \_ ENCADEAMENTO BCRYPT \_ | Algoritmos              | Standard  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ECB (Electronic Codebook)   | **\_ \_ ECB modo de cadeia de BCRYPT \_** | Codificações de bloco simétrico | SP800-38A |
| CBC (encadeamento de blocos de codificação) | **\_CBC do \_ modo de cadeia BCRYPT \_** | Codificações de bloco simétrico | SP800-38A |
| CFB (comentários cifrados)       | **CFB DO MODO CADEIA BCRYPT \_ \_ \_** | Codificações de bloco simétricas | SP800-38A |
| CCM (contador com CBC)      | **\_CCM DO MODO CADEIA BCRYPT \_ \_** | AES                     | SP800-38C |
| GCM (modo de contador/de contadores)   | **BCRYPT \_ CHAIN \_ MODE \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> Somente os modos de operação ECB, CBC e CFB são definidos Windows Vista. O GCM e o CCM Windows Vista com Service Pack 1 (SP1) ou Windows Server 2008.

 

 

 
