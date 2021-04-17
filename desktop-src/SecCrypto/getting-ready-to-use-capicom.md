---
description: Os aplicativos que usam objetos CAPICOM devem ser criados usando CAPICOM.dll. CAPICOM.dll também deve estar presente e registrado em tempo de execução para usar objetos CAPICOM.
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: Preparando-se para usar o CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769284"
---
# <a name="getting-ready-to-use-capicom"></a>Preparando-se para usar o CAPICOM

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Os aplicativos que usam objetos CAPICOM devem ser criados usando CAPICOM.dll. CAPICOM.dll também deve estar presente e registrado em tempo de execução para usar objetos CAPICOM. CAPICOM.dll deve ser adicionado a Visual Basic referências de projetos para usar objetos CAPICOM.

O CAPICOM está disponível como um arquivo redistribuível que pode ser baixado de [Platform SDK Redistributable: CApicom](https://www.microsoft.com/download/details.aspx?id=25281). Para obter informações sobre versões capicor, consulte [versões de capico](capicom-versions.md).

**Para registrar CAPICOM.dll**

-   Em um prompt de comando, altere o diretório para o diretório onde CAPICOM.dll está armazenado e, em seguida, digite o seguinte comando:

    **CAPICOM.dllregsvr32**

## <a name="example-code-limitations"></a>Limitações de código de exemplo

Para fornecer um código mais conciso e legível, os princípios de boa prática de programação nem sempre são seguidos nesses exemplos. Em particular, apenas respostas de erro limitadas são mostradas. Os aplicativos de trabalho sempre devem verificar os códigos de erro retornados e executar as ações apropriadas quando um erro for encontrado.

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>Contêineres de chave, chaves e certificados necessários no CAPICOM

Enquanto algumas operações com objetos CAPICOM podem ser feitas em qualquer computador por qualquer usuário, a criação de [*assinaturas digitais*](../secgloss/d-gly.md) e a recuperação do conteúdo de texto não criptografado de uma mensagem envelopada usando objetos CAPICOM são operações baseadas em certificado. O usuário que cria uma assinatura digital e o usuário que recupera o conteúdo criptografado de uma mensagem envelopada deve ter um certificado digital com uma chave privada associada disponível. Se um certificado com uma chave privada associada não estiver presente, a operação de criptografia falhará. Os usuários de aplicativos CAPICOM devem garantir que eles tenham o certificado apropriado e a chave privada disponível quando os aplicativos estiverem em execução.

Alguns exemplos nas seções a seguir executam operações que exigem um [*par de chaves pública/privada*](../secgloss/p-gly.md) disponível para criptografar e descriptografar arquivos, mensagens e assinaturas. Muitos desses programas serão compilados e executados, mas falharão em tempo de execução sem a existência de [*contêineres de chave*](../secgloss/k-gly.md), chaves, repositórios de certificados e [*certificados*](../secgloss/c-gly.md) apropriados nessas lojas.

**Para criar um certificado autoassinado**

1.  Instale as ferramentas de assinatura. Elas são instaladas como parte do SDK (Software Development Kit) do Microsoft Windows, do SDK (Kit de desenvolvimento de software) da plataforma ou do SDK do .NET Framework.
2.  Depois que Makecert.exe for baixado, execute o seguinte comando em um prompt de comando, substituindo um nome de usuário para *username*, um nome de organização para *OrganizationName* e um nome de empresa para *CompanyName*:

    **MakeCert-r-n "CN =**_username_*_, ou =_*_OrganizationName_*_, o =_*_CompanyName_*_" – SS My_*

3.  O certificado pode ser colocado no meu repositório do usuário atual. Importe o certificado criado no armazenamento raiz para que ele seja confiável.

 

 
