---
title: Cadeia de vinculação
description: Devido ao número de objetos acessíveis a partir de um serviço de diretório, podem ocorrer colisões de nomenclatura.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Cadeia de vinculação ADSI
- ADSI do ADsPath, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917669"
---
# <a name="binding-string"></a>Cadeia de vinculação

Devido ao número de objetos acessíveis a partir de um serviço de diretório, podem ocorrer colisões de nomenclatura. A cadeia de caracteres de associação, que é comumente conhecida como ADsPath, permite que você especifique um objeto específico sem causar uma colisão de nomenclatura. Isso pode ser aplicado a um único provedor de serviços de diretório ou a vários provedores de serviço de diretório.

Um ADsPath é uma cadeia de caracteres que identifica exclusivamente um objeto ADSI em um serviço de diretório. Como os objetos ADSI existem dentro do contexto do namespace do serviço de diretório subjacente, parte da sintaxe de um nome ADsPath é específica do provedor.

A tabela a seguir lista os provedores ADSI fornecidos por padrão.



| Provedor         | Descrição                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | Usado para se comunicar com os controladores de domínio do Windows. Para obter mais informações sobre o ADsPath WinNT, consulte o [ADsPath do Winnt](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Usado para se comunicar com servidores LDAP, como Active Directory. Para obter mais informações sobre o ADsPath LDAP, consulte o [ADsPath LDAP](ldap-adspath.md).<br/>  |
| Banner<br/>   | Fornece uma implementação de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que pode ser usada para enumerar todos os provedores ADSI instalados no cliente.<br/> |



 

Use esses nomes de provedor para acessar o namespace do provedor padrão. Por exemplo, se você associar ao LDAP, a ADSI ligará a um contêiner que contém o objeto de domínio conectado no momento. Se você associar ao WinNT, a ADSI será vinculada a um contêiner que contém objetos que se correlacionam a todos os domínios na rede.

Os elementos iniciais da cadeia de caracteres ADsPath são o identificador programático (progID) do provedor ADSI, seguido por "://", seguido pela sintaxe ditada pelo namespace do provedor. A cadeia de caracteres progID pode ou não diferenciar maiúsculas de minúsculas, dependendo do provedor. As cadeias de caracteres progID para os provedores listados acima diferenciam maiúsculas de minúsculas.

A cadeia de caracteres de caminho pode ou não diferenciar maiúsculas de minúsculas, dependendo do provedor. As cadeias de caracteres de caminho para os provedores listados acima não diferenciam maiúsculas de minúsculas.

Veja a seguir exemplos de ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Para localizar todos os provedores instalados em seu computador, associe-se ao provedor ADs, conforme mostrado no exemplo de código a seguir.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Usando o provedor LDAP, você pode especificar o ADsPath em um formulário DN (nome diferenciado) X. 500, começando com a marca CN ou pode especificar seu inverso hierárquico, começando com a marca o. O formulário que você usa no ADsPath inicial determina a ordem das marcas.

A tabela a seguir lista os caracteres especiais ADsPath.



| Nome                      | Caractere           | Descrição                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aspas duplas<br/>   | "<br/>        | Usado para citar qualquer parte do ADsPath que possa conter um caractere especial para que a cadeia de caracteres seja interpretada literalmente. Por exemplo, "CN = Nome/prefixo".<br/>                                     |
| Barra invertida<br/>      | \\<br/>       | Usado para preceder caracteres especiais para significar que eles devem ser usados como literais. Para obter mais informações e uma lista de caracteres especiais, consulte [nomes distintos](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| Caractere<br/>          | /<br/>        | Separador de componentes.<br/>                                                                                                                                                                       |
| Colchetes angulares<br/> | <><br/> | Delimite um ADsPath dentro de outra convenção de nomenclatura.<br/>                                                                                                                                       |



 

Para delimitar um ADsPath em uma especificação de pesquisa ou como parte de uma URL, use o colchete angular esquerdo e direito (< >). Por exemplo, " &lt; winnt://mydomain/UserAccount &gt; ".

Alguns provedores ADSI podem ter as restrições de sintaxe adicionadas devido a requisitos de namespace.

## <a name="active-directory-binding-options"></a>Opções de associação de Active Directory

Active Directory fornece a capacidade de associar a um objeto usando vários outros tipos de cadeias de caracteres de associação, como um GUID (identificador global exclusivo) de COM ou um SID (identificador de segurança). Para obter mais informações, consulte [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

