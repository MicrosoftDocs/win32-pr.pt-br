---
title: LDAP ADsPath
description: Este tópico mostra a sintaxe que você deve usar para o LDAP ADsPath.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP ADsPath
- ADsPath, LDAP, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1850c30ff8a5a086fbd697080ac32b5e55549496739d9388a6d5e7ab251403d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839466"
---
# <a name="ldap-adspath"></a>LDAP ADsPath

O ADsPath do provedor LDAP da Microsoft requer o formato a seguir.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Os caracteres de colchete esquerdo e direito ( \[ \] ) indicam parâmetros opcionais; ele não é uma parte literal da cadeia de caracteres de associação.

 

O "HostName" pode ser um nome de computador, um endereço IP ou um nome de domínio. Um nome de servidor também pode ser especificado na cadeia de caracteres de associação. A maioria dos provedores LDAP segue um modelo que exige que um nome de servidor seja especificado.

O "PortNumber" especifica a porta a ser usada para a conexão. Se nenhum número de porta for especificado, o provedor LDAP usará o número da porta padrão. O número da porta padrão será 389 se não estiver usando uma conexão SSL ou 636 se estiver usando uma conexão SSL.

O "DistinguishedName" especifica o nome diferenciado de um objeto específico. Um nome diferenciado para um determinado objeto tem a garantia de ser exclusivo.

A tabela a seguir lista exemplos de cadeias de caracteres de associação.



| Exemplo de LDAP ADsPath                                      | Descrição                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| Ldap:                                                     | A bind à raiz do namespace LDAP.                    |
| LDAP://server01                                           | A vincular a um servidor específico.                                 |
| LDAP://server01:390                                       | A bind a um servidor específico usando o número da porta especificado. |
| LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com          | A vincular a um objeto específico.                                 |
| LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com | A vincular a um objeto específico por meio de um servidor específico.       |



 

Se a autenticação Kerberos for necessária para a conclusão bem-sucedida de uma solicitação de diretório específica, a cadeia de caracteres de associação deverá usar um ADsPath sem servidor, como LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com ou deve usar um ADsPath com um nome de servidor DNS totalmente qualificado, como LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com. A associação ao servidor usando um nome NETBIOS simples ou um nome DNS curto, por exemplo, usando o nome server01 em vez de server01.fabrikam.com, não tem garantia de que produzirá a autenticação Kerberos.

Para obter mais informações e exemplos de cadeias de caracteres de associação LDAP, bem como uma descrição de caracteres especiais que podem ser usados em cadeias de caracteres de associação LDAP, consulte LDAP ADsPath.

**Windows 2000 com SP1 e posterior:** Com o provedor LDAP, se uma cadeia de caracteres de associação incluir um nome de servidor, você poderá aumentar o desempenho usando o sinalizador **ADS \_ SERVER \_ BIND** com a [**função ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) O **sinalizador ADS SERVER \_ \_ BIND** indica que um nome de servidor foi especificado, o que permite que a ADSI evite tráfego de rede adicional e desnecessário.

## <a name="ldap-special-characters"></a>Caracteres especiais LDAP

O LDAP tem vários caracteres especiais que são reservados para uso pela API LDAP. A lista de caracteres especiais pode ser encontrada em [Nomes Diferenciados.](/previous-versions/windows/desktop/ldap/distinguished-names) Para usar um desses caracteres em um ADsPath sem gerar um erro, o caractere deve ser precedido por um caractere de invertida ( \\ ). Isso é conhecido como *escape do* caractere. Por exemplo, se um nome de usuário for dado na forma de " , ", a vírgula no valor <last name> de nome deverá ser <first name> escapada. A cadeia de caracteres resultante teria esta aparência:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



O caractere de escape também pode ser especificado por seu código de caractere hexadecimal de dois dígitos. Isso é mostrado no exemplo a seguir.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Caracteres não imprimíveis, como alimentação de linha e retorno de carro, devem ser escapados e especificados pelo código de caractere hexadecimal de dois dígitos. Isso é mostrado no exemplo a seguir.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Para obter mais informações

Para obter mais informações sobre a notação de nome diferenciado usada pelos serviços de diretório compatíveis com LDAP, consulte [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 