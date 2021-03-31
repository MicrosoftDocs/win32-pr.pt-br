---
title: Associação a objetos Well-Known usando WKGUID
description: Este tópico mostra como associar objetos usando a cadeia de caracteres de associação WKGUID.
ms.assetid: cc9846c4-415e-48ee-ae08-6631636d3a63
ms.tgt_platform: multiple
keywords:
- Associação a objetos de Well-Known usando o AD WKGUID
- Active Directory, usando, associação, usando WKGUID para associar a objetos bem conhecidos
- objetos conhecidos do AD
- objetos conhecidos do AD, ligando-se ao usando WKGUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd919efa6e52d7e65c2a7cd5550f3d217f54070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640436"
---
# <a name="binding-to-well-known-objects-using-wkguid"></a>Associação a objetos Well-Known usando WKGUID

Os contêineres podem ter um ou mais subobjetos importantes que podem ser renomeados ou movidos. Pode ser difícil controlar esses subobjetos e criar cadeias de vinculação corretas para eles, especialmente se eles forem renomeados ou movidos.

Para dar suporte à associação de renomeação segura a esses objetos dentro desses contêineres, Active Directory Domain Services têm dois atributos: **wellKnownObjects** e **otherWellKnownObjects**. Esses atributos têm uma sintaxe de atributo de \_ DN ADSTYPE \_ com \_ Binary. Eles permitem vários valores e contêm as tuplas GUID/DN de objetos bem conhecidos dentro dos contêineres nos quais eles estão definidos. O servidor de Active Directory mantém a parte do nome distinto de cada entrada **wellKnownObjects** e **otherWellKnownObjects** para que ela contenha o nome distinto atual do objeto especificado quando a entrada foi criada.

A propriedade **otherWellKnownObjects** pode ser definida e usada em qualquer objeto.

A propriedade **wellKnownObjects** é usada nos contêineres de configuração e DomainDNS. A propriedade **wellKnownObjects** é uma propriedade somente do sistema e só pode ser modificada pelo sistema operacional.

O contêiner **domainDns** tem os seguintes objetos bem conhecidos:

-   Usuários
-   Computadores
-   Sistema
-   Controladores de Domínio
-   Infraestrutura
-   Objetos excluídos
-   Perdidos e encontrados

O contêiner de configuração tem o objeto bem conhecido: objetos excluídos.

Esses objetos estão em cada **domainDns** e contêiner de configuração em um serviço domínio do Active Directory.

Você pode associar a um objeto conhecido usando o formato de associação WKGUID. Só há suporte para associação com WKGUID em Active Directory Domain Services, ou seja, o provedor LDAP.

> [!IMPORTANT]
> Sempre use o formato de associação WKGUID para se associar aos objetos conhecidos, conforme listado acima, nos contêineres de domínio e configuração. Isso garante que esses contêineres possam ser associados mesmo se forem movidos ou renomeados.

 

O formato da cadeia de vinculação WKGUID é o seguinte:


```C++
LDAP://<servername>/<WKGUID=<XXXXX>,<container DN>>
```



" &lt; nome do servidor &gt; " é o nome do servidor de diretório. O " &lt; nome do servidor &gt; " é opcional.

" &lt; Xxxxx &gt; " é a representação de cadeia de caracteres do valor HEXADECIMAL do GUID que representa o objeto bem conhecido. A cadeia de caracteres GUID é especificada no formulário "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" e não é a mesma forma que a cadeia de caracteres GUID produzida pela função [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , que usa o formato "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}". Para obter mais informações e um exemplo de código que mostra como criar uma cadeia de caracteres vinculável de um GUID, consulte [exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).

Para associar a um objeto especificado em **otherWellKnownObjects** em um objeto, especifique " &lt; xxxxx &gt; " como a forma de cadeia de caracteres de associação do GUID de objeto conhecido do objeto. Para obter mais informações, consulte [lendo o OBJECTguid de um objeto e criando uma representação de cadeia de caracteres do GUID](reading-an-objectampaposs-objectguid-and-creating-a-string-representation-of-the-guid.md). Para obter mais informações sobre como definir a propriedade **otherWellKnownObjects** em objetos, consulte [habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md).

Para associar a um objeto especificado em **wellKnownObjects** em domainDns ou contêineres de configuração, especifique " &lt; xxxxx &gt; " como uma das constantes a seguir, listadas na tabela a seguir, conforme definido em NTDSAPI. h.



| Contêiner          | Identificador GUID                         |
|--------------------|-----------------------------------------|
| Usuários              | \_contêiner de usuários GUID \_ \_ W               |
| Computadores          | \_contêiner COMPUTRS \_ GUID \_ W            |
| Sistema             | contêiner de sistemas de GUID \_ \_ \_ W             |
| Controladores de Domínio | contêiner de controladores de domínio do GUID \_ \_ \_ \_ W |
| Infraestrutura     | contêiner de infraestrutura de GUID \_ \_ \_ W      |
| Objetos excluídos    | \_contêiner de objetos excluídos de GUID \_ \_ \_ W    |
| Perdidos e encontrados     | contêiner de LOSTANDFOUND de GUID \_ \_ \_ W        |



 

Por exemplo, para associar ao contêiner de usuário em um domínio, especifique **o \_ contêiner de usuários GUID \_ \_ W** como " &lt; xxxxx &gt; ".

" &lt; container DN &gt; " é o nome distinto do objeto de contêiner que tem esse objeto representado como um valor em sua propriedade **wellKnownObjects** . Por exemplo, para associar ao contêiner usuários em um domínio, especifique o nome distinto do domínio como o " &lt; DN do contêiner &gt; ".

Por exemplo, para associar ao contêiner usuários do domínio Fabrikam.com, use a cadeia de vinculação a seguir.

``` syntax
LDAP://<WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=Fabrikam,dc=com>
```

Para obter mais informações e um exemplo de código que mostra como associar a um GUID bem conhecido, consulte [código de exemplo para associação a objetos bem conhecidos](example-code-for-binding-to-well-known-objects.md).

 

 