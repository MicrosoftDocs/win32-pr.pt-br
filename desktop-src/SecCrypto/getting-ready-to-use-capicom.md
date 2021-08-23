---
description: Os aplicativos que usam objetos CAPICOM devem ser criados usando CAPICOM.dll. CAPICOM.dll deve estar presente e registrado em tempo de executar para usar objetos CAPICOM.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Preparando-se para usar CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a6b76c293395fd0979cf5c304b27bae75622996279bd891b8c0c1301dca82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006624"
---
# <a name="getting-ready-to-use-capicom"></a>Preparando-se para usar CAPICOM

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Os aplicativos que usam objetos CAPICOM devem ser criados usando CAPICOM.dll. CAPICOM.dll deve estar presente e registrado em tempo de executar para usar objetos CAPICOM. CAPICOM.dll devem ser adicionadas a Visual Basic de projetos para usar objetos CAPICOM.

CAPICOM está disponível como um arquivo redistribuível que pode ser baixado do [SDK da Plataforma Redistribuível: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281). Para obter informações sobre as versões do CAPICOM, consulte [Versões do CAPICOM.](capicom-versions.md)

**Para registrar CAPICOM.dll**

-   Em um prompt de comando, altere o diretório para o diretório onde CAPICOM.dll está armazenado e digite o seguinte comando:

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>Limitações de código de exemplo

Para fornecer um código mais conciso e acessível, os princípios de uma boa prática de programação nem sempre são seguidos nesses exemplos. Em particular, apenas respostas de erro limitadas são mostradas. Os aplicativos de trabalho sempre devem verificar os códigos de erro retornados e executar as ações apropriadas quando um erro é encontrado.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contêineres de chave, chaves e certificados necessários no CAPICOM

Embora algumas operações com objetos CAPICOM possam ser feitas em qualquer computador por qualquer usuário, a criação de assinaturas digitais e a recuperação do conteúdo de texto não criptografado de uma mensagem envelizada usando objetos CAPICOM são operações [*baseadas*](../secgloss/d-gly.md) em certificado. O usuário que cria uma assinatura digital e o usuário que recupera o conteúdo criptografado de uma mensagem envelizada deve ter um certificado digital com uma chave privada associada disponível. Se um certificado com uma chave privada associada não estiver presente, a operação criptográfica falhará. Os usuários de aplicativos CAPICOM devem garantir que tenham o certificado apropriado e a chave privada disponível quando os aplicativos estão em execução.

Alguns exemplos nas seções a seguir executam operações que exigem um par de chaves [*pública/privada*](../secgloss/p-gly.md) disponível para criptografar e descriptografar arquivos, mensagens e assinaturas. Muitos desses programas serão compilados e executados, mas falharão em tempo de operação sem a existência de contêineres de chave [*adequados,*](../secgloss/k-gly.md)chaves, armazenamentos de certificados e [*certificados*](../secgloss/c-gly.md) nesses armazenamentos.

**Para criar um certificado autoassinado**

1.  Instale as ferramentas de assinatura. Eles são instalados como parte do SDK (Software Development Kit) do Microsoft Windows, do SDK (Kit de Desenvolvimento de Software de Plataforma) ou do SDK do .NET Framework.
2.  Depois Makecert.exe baixado, execute o seguinte comando em um prompt de comando, substituindo um nome de usuário para *UserName*, um nome de organização para *OrganizationName* e um nome de empresa para *CompanyName*:

    **makecert -r -n "cn=**_UserName_*_, ou=_*_OrganizationName_*_, o=_*_CompanyName"_*_-ss my_*

3.  O certificado pode ser colocado no Meu armazenamento do usuário atual. Importe o certificado criado para o armazenamento raiz para que ele seja confiável.

 

 
