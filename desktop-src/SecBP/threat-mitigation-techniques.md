---
description: Há várias técnicas de mitigação de ameaças disponíveis que podem ser usadas para proteger melhor as senhas.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Técnicas de mitigação de ameaças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315a79ec1db48a16de858d655bd1550fa1458720
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482442"
---
# <a name="threat-mitigation-techniques"></a>Técnicas de mitigação de ameaças

Há várias técnicas de mitigação de ameaças disponíveis que podem ser usadas para proteger melhor as senhas. Essas técnicas são implementadas usando uma ou mais das quatro principais tecnologias a seguir.



| Tecnologia                      | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | O CryptoAPI fornece um conjunto de funções que ajudam a aplicar rotinas de criptografia às entidades de destino. A CryptoAPI pode fornecer hashes, resumos, criptografia e descriptografia, para mencionar sua funcionalidade principal. O CryptoAPI também tem outros recursos. Para saber mais sobre criptografia e a CryptoAPI, consulte [noções básicas sobre criptografia](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Listas de controle de acesso            | Uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) é uma lista de proteções de segurança que se aplica a um objeto. Um objeto pode ser um arquivo, processo, evento ou qualquer outra coisa que tenha um descritor de segurança. Para obter mais informações sobre ACLs, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists) (ACLs). |
| API de proteção de dados             | A API de proteção de dados (DPAPI) fornece as quatro funções a seguir que você usa para criptografar e descriptografar dados confidenciais: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)e [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Nomes de usuário e senhas armazenados | Armazenamento funcionalidade que torna o tratamento de senhas de usuários e outras credenciais, como chaves privadas, mais fáceis, consistentes e mais seguras. Para obter mais informações sobre essa funcionalidade, consulte [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).                                                                                                         |



 

Essas tecnologias não estão disponíveis em todos os sistemas operacionais. Portanto, a extensão para a qual a segurança pode ser aprimorada depende de quais sistemas operacionais estão envolvidos. Aqui estão as tecnologias que estão disponíveis em cada sistema operacional.


| Sistema operacional | Tecnologia | 
|------------------|------------|
| Windows Server 2003 e Windows XP | <ul><li>CryptoAPI</li><li>Listas de controle de acesso</li><li>API de proteção de dados</li><li>Nomes de usuário e senhas armazenados</li></ul> | 
| Windows 2000 | <ul><li>CryptoAPI</li><li>Listas de controle de acesso</li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li></ul> | 




 

As seguintes técnicas de mitigação de ameaças usam uma ou mais das quatro tecnologias. As técnicas que exigem o uso de tecnologias que não estão incluídas no sistema operacional não podem ser usadas.

## <a name="getting-passwords-from-the-user"></a>Obtendo senhas do usuário

Quando você permite que o usuário configure uma senha, Force o uso de senhas fortes. Por exemplo, exigir que as senhas tenham um comprimento mínimo, como oito caracteres ou mais. As senhas também devem ser necessárias para incluir letras maiúsculas e minúsculas, números e outros caracteres de teclado, como o cifrão ($), ponto de exclamação (!) ou maior que (>).

Depois de obter uma senha, use-a rapidamente (usando o mínimo de código possível) e, em seguida, apague todas as eliminemos da senha. Isso minimiza o tempo disponível para um invasor "interceptar" a senha. A desvantagem dessa técnica é a frequência com a qual a senha deve ser recuperada do usuário; no entanto, o princípio deve ser empregado sempre que possível. Para obter informações sobre como obter senhas corretamente, consulte [solicitando credenciais ao usuário](asking-the-user-for-credentials.md).

Evite fornecer opções de interface do usuário "lembrar minha senha". Muitas vezes, os usuários exigirão ter essa opção. Se você precisar fornecê-lo, no mínimo, certifique-se de que a senha seja salva de maneira segura. Para obter informações, consulte a seção Armazenando senhas, mais adiante neste tópico.

Limitar tentativas de entrada de senha. Após um determinado número de tentativas sem êxito, bloqueie o usuário por um determinado período de tempo. Opcionalmente, aumente o tempo de resposta para cada tentativa acima de um máximo. Essa técnica se destina a anular um ataque de adivinhação.

## <a name="storing-passwords"></a>Armazenando senhas

Nunca armazene senhas em texto não criptografado (sem criptografia). A criptografia de senhas aumenta significativamente sua segurança. Para obter informações sobre como armazenar senhas criptografadas, consulte [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Para obter informações sobre como criptografar senhas na memória, consulte [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Armazene senhas no mínimo de lugares possível. Quanto mais locais uma senha estiver armazenada, maior será a chance de que um intruso possa encontrá-la. Nunca armazene as senhas em uma página da Web ou em um arquivo baseado na Internet. O armazenamento de senhas em uma página da Web ou em um arquivo de base permite que elas sejam facilmente comprometidas.

Depois de criptografar uma senha e armazená-la, use ACLs seguras para limitar o acesso ao arquivo. Como alternativa, você pode armazenar senhas e chaves de criptografia em dispositivos removíveis. O armazenamento de senhas e chaves de criptografia em uma mídia removível, como um cartão inteligente, ajuda a criar um sistema mais seguro. Depois que uma senha é recuperada para uma determinada sessão, o cartão pode ser removido, removendo, assim, a possibilidade de que um invasor possa obter acesso a ele.

 

 
