---
title: Cadeia de caracteres de associação
description: Devido ao número de objetos acessíveis de um serviço de diretório, podem ocorrer colisões de nomeação.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI da cadeia de caracteres de associação
- ADSI do ADsPath, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8e1bc59011c1279b340348572fa0681a0d301319f75603b73714df4c9cb96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023684"
---
# <a name="binding-string"></a>Cadeia de caracteres de associação

Devido ao número de objetos acessíveis de um serviço de diretório, podem ocorrer colisões de nomeação. A cadeia de caracteres de associação, que normalmente é conhecida como ADsPath, permite que você especifique um objeto específico sem causar uma colisão de nomeação. Isso pode ser aplicado a um provedor de serviços de diretório único ou em vários provedores de serviços de diretório.

Um ADsPath é uma cadeia de caracteres que identifica exclusivamente um objeto ADSI em um serviço de diretório. Como os objetos ADSI existem dentro do contexto do namespace do serviço de diretório subjacente, parte da sintaxe de um nome ADsPath é específica do provedor.

A tabela a seguir lista os provedores ADSI fornecidos por padrão.



| Provedor         | Descrição                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winnt<br/> | Usado para se comunicar com Windows controladores de domínio. Para obter mais informações sobre o WinNT ADsPath, consulte [WinNT ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Usado para se comunicar com servidores LDAP, como o Active Directory. Para obter mais informações sobre o LDAP ADsPath, consulte [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Anúncios<br/>   | Fornece uma [**implementação IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que pode ser usada para enumerar todos os provedores ADSI instalados no cliente.<br/> |



 

Use esses nomes de provedor para acessar o namespace do provedor padrão. Por exemplo, se você se vincular ao LDAP, a ADSI será vinculada a um contêiner que contém o objeto de domínio conectado no momento. Se você se vincular ao WinNT, a ADSI será vinculada a um contêiner que contém objetos que se correlacionam a todos os domínios na rede.

Os elementos iniciais da cadeia de caracteres ADsPath são o progID (identificador programático) do provedor ADSI, seguido por "://", seguido pela sintaxe ditada pelo namespace do provedor. A cadeia de caracteres progID pode ou não ser sensível a minúsculas, dependendo do provedor. As cadeias de caracteres progID para os provedores listados acima são sensíveis a minúsculas.

A cadeia de caracteres de caminho pode ou não ser sensível a minúsculas, dependendo do provedor. As cadeias de caracteres de caminho para os provedores listados acima não são sensíveis a minúsculas.

A seguir estão exemplos de ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Para encontrar todos os provedores instalados no computador, a bind ao provedor do ADS, conforme mostrado no exemplo de código a seguir.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Usando o provedor LDAP, você pode especificar o ADsPath em um formato DN (nome diferenciado) X.500, começando com a marca CN ou pode especificar seu inverso hierárquico, começando com a marca O. O formulário usado no ADsPath inicial determina a ordem das marcas.

A tabela a seguir lista caracteres especiais ADsPath.



| Nome                      | Caractere           | Descrição                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aspas duplas<br/>   | "<br/>        | Usado para citar qualquer parte do ADsPath que possa conter um caractere especial para que a cadeia de caracteres seja interpretada literalmente. Por exemplo, "CN=Name/Prefix".<br/>                                     |
| Barra invertida<br/>      | \\<br/>       | Usado para preceder caracteres especiais para significar que eles devem ser usados como literais. Para obter mais informações e uma lista de caracteres especiais, consulte [Nomes diferenciados.](/previous-versions/windows/desktop/ldap/distinguished-names)<br/> |
| Barra<br/>          | /<br/>        | Separador de componente.<br/>                                                                                                                                                                       |
| Colchetes angulares<br/> | <><br/> | Delimituar um ADsPath dentro de outra convenção de nomenminação.<br/>                                                                                                                                       |



 

Para delimitar um ADsPath em uma especificação de pesquisa ou como parte de uma URL, use o colchete angular esquerdo e direito (< >). Por exemplo, " &lt; WinNT://MyDomain/UserAccount &gt; ".

Alguns provedores ADSI podem ter adicionado restrições de sintaxe devido aos requisitos de namespace.

## <a name="active-directory-binding-options"></a>Opções de associação do Active Directory

O Active Directory fornece a capacidade de se vincular a um objeto usando vários outros tipos de cadeias de caracteres de associação, como um GUID (identificador global exclusivo) COM ou um SID (identificador de segurança). Para obter mais informações, consulte [Associação ao Active Directory.](/windows/desktop/AD/binding-to-active-directory-domain-services)

 

