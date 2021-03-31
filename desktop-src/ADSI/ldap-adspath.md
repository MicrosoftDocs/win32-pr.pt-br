---
title: ADsPath LDAP
description: Este tópico mostra a sintaxe que você deve usar para o ADsPath do LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- ADsPath LDAP
- ADsPath, LDAP, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641851"
---
# <a name="ldap-adspath"></a>ADsPath LDAP

O ADsPath do provedor LDAP da Microsoft requer o seguinte formato.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Os caracteres de colchetes esquerdo e direito ( \[ \] ) indicam parâmetros opcionais; não é uma parte literal da cadeia de caracteres de associação.

 

O "HostName" pode ser um nome de computador, um endereço IP ou um nome de domínio. Um nome de servidor também pode ser especificado na cadeia de vinculação. A maioria dos provedores LDAP segue um modelo que exige a especificação de um nome de servidor.

A "PortNumber" especifica a porta a ser usada para a conexão. Se nenhum número de porta for especificado, o provedor LDAP usará o número da porta padrão. O número da porta padrão será 389 se não estiver usando uma conexão SSL ou 636 se estiver usando uma conexão SSL.

O "DistinguishedName" especifica o nome distinto de um objeto específico. É garantido que um nome distinto para um determinado objeto seja exclusivo.

A tabela a seguir lista exemplos de cadeias de caracteres de associação.



| Exemplo de ADsPath LDAP                                      | Descrição                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| LDAP                                                     | Associar à raiz do namespace LDAP.                    |
| LDAP://server01                                           | Associar a um servidor específico.                                 |
| LDAP://server01:390                                       | Associar a um servidor específico usando o número da porta especificada. |
| LDAP:Binding = Jeff Smith, CN = Users, DC = Fabrikam, DC = com          | Associar a um objeto específico.                                 |
| LDAP://server01/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com | Associar a um objeto específico por meio de um servidor específico.       |



 

Se a autenticação Kerberos for necessária para a conclusão bem-sucedida de uma solicitação de diretório específica, a cadeia de vinculação deverá usar um ADsPath sem servidor, como LDAP:Binding = Jeff Smith, CN = Users, DC = Fabrikam, DC = com ou deve usar um ADsPath com um nome de servidor DNS totalmente qualificado, como LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com. A associação ao servidor usando um nome NETBIOS simples ou um nome DNS curto, por exemplo, usando o nome Server01 em vez de server01.fabrikam.com, não é garantida para produzir a autenticação Kerberos.

Para obter mais informações e exemplos de cadeias de vinculação LDAP, bem como uma descrição de caracteres especiais que podem ser usados em cadeias de vinculação LDAP, consulte ADsPath LDAP.

**Windows 2000 com SP1 e posterior:** Com o provedor LDAP, se uma cadeia de vinculação incluir um nome de servidor, você poderá aumentar o desempenho usando o sinalizador de **\_ \_ associação do servidor ADS** com a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . O sinalizador de **\_ \_ ligação do servidor ADS** indica que um nome de servidor foi especificado, o que permite que a ADSI Evite tráfego de rede adicional e desnecessário.

## <a name="ldap-special-characters"></a>Caracteres especiais do LDAP

O LDAP tem vários caracteres especiais que são reservados para uso pela API LDAP. A lista de caracteres especiais pode ser encontrada em [nomes distintos](/previous-versions/windows/desktop/ldap/distinguished-names). Para usar um desses caracteres em um ADsPath sem gerar um erro, o caractere deve ser precedido por um caractere de barra invertida ( \\ ). Isso é conhecido como *escapar* do caractere. Por exemplo, se um nome de usuário for fornecido na forma de " <last name> , <first name> ", a vírgula no valor de nome deverá ter escape. A cadeia de caracteres resultante ficaria assim:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



O caractere de escape também pode ser especificado por seu código de caractere hexadecimal de dois dígitos. Isso é mostrado no exemplo a seguir.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Os caracteres não imprimíveis, como a alimentação de linha e o retorno de carro, devem ser inseridos e especificados pelo código de caractere hexadecimal de dois dígitos. Isso é mostrado no exemplo a seguir.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Para obter mais informações

Para obter mais informações sobre a notação de nome distinto usada por serviços de diretório compatíveis com LDAP, consulte [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 