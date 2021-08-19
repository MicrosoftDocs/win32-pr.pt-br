---
title: Criando uma partição de diretório do aplicativo
description: Uma partição de diretório de aplicativo é representada por um objeto domainDNS com um valor de atributo instanceType de DS INSTANCETYPE IS NC HEAD combinado com \_ \_ \_ \_ DS \_ INSTANCETYPE \_ NC É \_ \_ WRITEABLE.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Criando um AD de Partição do Diretório do Aplicativo
- AD de partições do diretório de aplicativos, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c340bac215be62867dcddcda97326c33fc70c458ee242965258cc1ee24cf25f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020535"
---
# <a name="creating-an-application-directory-partition"></a>Criando uma partição de diretório do aplicativo

Uma partição de diretório de aplicativo é representada por um objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) com um valor de atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) de **DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** combinado com **DS \_ INSTANCETYPE NC É \_ \_ \_ WRITEABLE**. Esse **objeto domainDNS** representa a raiz da partição do diretório do aplicativo (cabeça nc) e é nomeado como semelhante a uma partição de domínio regular, por exemplo, "DC=dynamicdata,DC=fabrikam,DC=com", que corresponde a um nome DNS de "dynamicdata.fabrikam.com". Uma partição de diretório do aplicativo pode, portanto, ser instautada em qualquer lugar em que uma partição de domínio possa ser instautada. Não há nenhum nome NetBIOS associado a uma partição de diretório do aplicativo.

É possível aninhar partições de diretório do aplicativo, ou seja, uma partição de diretório do aplicativo pode ter partições de diretório de aplicativo filho. Pesquisas com escopo de subárvore com raiz em um cabeça de partição do diretório do aplicativo gerarão referências de continuação para as partições de diretório do aplicativo filho.

Uma réplica de partição de diretório de aplicativo só pode ser criada em um controlador de domínio que está em execução no Windows Server 2003 e posterior e somente enquanto a função FSMO do Domain-Naming é mantida por um controlador de domínio Windows Server 2003 e posterior. Em uma floresta mista que tenha controladores de domínio do Windows Server 2003 e controladores de domínio de nível inferior (controladores de domínio do Windows 2000 ou controladores de domínio primário do Windows NT 4.0), uma tentativa de criar uma réplica de partição de diretório do aplicativo em um controlador de domínio de nível inferior falhará.

Uma partição de diretório do aplicativo também tem um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) correspondente no contêiner Partições da partição de configuração. O **crossRef** pode ser pré-criado manualmente antes de criar o [**objeto domainDNS.**](/windows/desktop/ADSchema/c-domaindns) O objeto **crossRef** criado previamente deve ter os valores de atributo mostrados na tabela a seguir ou a criação da partição falhará. Se o **objeto crossRef** não existir, o servidor do Active Directory criará um quando a partição do diretório do aplicativo for criada.

| Atributo                          | Descrição                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dnsroot**](/windows/desktop/ADSchema/a-dnsroot) | Contém o caminho DNS do controlador de domínio no qual a partição de diretório do aplicativo será criada.                               |
| [**habilitado**](/windows/desktop/ADSchema/a-enabled) | Contém **FALSE.**                                                                                                                       |
| [**Ncname**](/windows/desktop/ADSchema/a-ncname)   | Contém o nome diferenciado da partição. No exemplo acima, esse atributo conteria "DC=dynamicdata,DC=mydomain,DC=com". |



 

**Para criar uma nova partição de diretório de aplicativo com sua primeira réplica, execute as etapas a seguir**

1.  A bind ao namespace da nova partição, especificando o controlador de domínio que hospedará a partição de diretório do aplicativo no ADsPath. Por exemplo, para criar uma partição com um ADsPath de "DC=dynamicdata,DC=mydomain,DC=com", a associação ADsPath seria "LDAP:// <domain controller> /DC=mydomain,DC=com", em que " controlador de domínio " é o nome DNS do controlador de domínio que hospedará a &lt; &gt; partição.

    A operação de vinculação deve especificar as opções rápidas e de delegação. A opção rápida permite que a vinculação seja bem-sucedida mesmo que o namespace não exista. A opção de delegação é necessária para permitir que o controlador de domínio entre em contato com o proprietário da função Domain-Naming FSMO usando as mesmas credenciais.

    A versão do sistema do controlador de domínio deve ser Windows sistema operacional Server 2003 e posterior.

2.  Crie um [**objeto domainDNS**](/windows/desktop/ADSchema/c-domaindns) com um nome apropriado para a partição, por exemplo, "DC=dynamicdata", para representar o head de contexto de nomentura para a nova partição. O **objeto domainDNS** deve ter um atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) com um valor de 5 (**DS \_ INSTANCETYPE IS NC \_ \_ \_ HEAD** \| **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE**). O **atributo instanceType** só pode ser definido no momento da criação porque é um atributo somente do sistema.

Quando o [**objeto domainDNS**](/windows/desktop/ADSchema/c-domaindns) for criado, o servidor do Active Directory executará as seguintes etapas:

1.  Pesquisa um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) no contêiner Partitions que tem um valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que corresponde ao nome diferenciado da partição e, se uma corresponder for encontrada, modificará o objeto **crossRef** para representar a partição de diretório do aplicativo. Se um objeto **crossRef** correspondente não for encontrado, o servidor do Active Directory criará um novo **objeto crossRef** para representar a partição do diretório do aplicativo.

    A tabela a seguir lista atributos importantes do [**objeto crossRef.**](/windows/desktop/ADSchema/c-crossref)

    | Atributo                                                              | Descrição                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**Ncname**](/windows/desktop/ADSchema/a-ncname)                                       | Contém o nome diferenciado da partição.                                                                                                  |
    | [**Dnsroot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contém o nome DNS da partição.                                                                                                            |
    | [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | O nome diferenciado do [**objeto nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) do controlador de domínio para a primeira réplica é adicionado a esse atributo. |

    

     

2.  Inicie uma sincronização da partição de configuração e aguarde a conclusão. Isso permite que o aplicativo cliente modifique parâmetros de configuração para a partição de diretório do aplicativo recém-criada enquanto estiver vinculado ao mesmo controlador de domínio usado para criar a partição de diretório do aplicativo.
3.  Crie o [**objeto domainDNS**](/windows/desktop/ADSchema/c-domaindns) com os sinalizadores **DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** e **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE** definidos na [**propriedade instanceType.**](/windows/desktop/ADSchema/a-instancetype) A **propriedade instanceType** também pode conter outros sinalizadores privados.
4.  Preencha o atributo [**ms-DS-Has-Master-NCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para o controlador de domínio de destino com o nome diferenciado da partição de diretório do aplicativo recém-criada.

Quando a partição do diretório do aplicativo é criada ou quando uma nova réplica da partição de diretório do aplicativo é adicionada e totalmente sincronizada, o servidor do Active Directory registra corretamente a réplica com NetLogon e DNS. Para obter mais informações e uma lista dos registros SRV registrados, consulte Localizando um servidor host de [partição do diretório do aplicativo.](locating-an-application-directory-partition-host-server.md)

Para obter mais informações sobre como criar uma partição de diretório do aplicativo, consulte [Código de exemplo para criar uma partição de diretório do aplicativo](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Localizando o contêiner de partições

O nome diferenciado do contêiner Partições pode ser encontrado de duas maneiras. A primeira é mais complicada de executar, mas sempre fornecerá um resultado preciso:

1.  Agresse a RootDSE e obtenha o **atributo configurationNamingContext.**
2.  Use o **atributo configurationNamingContext** para se vincular ao contêiner de configuração.
3.  Pesquise no contêiner de configuração um objeto do tipo [**crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)
4.  Obtenha o valor do atributo **distinguishedName** do [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer) Esse será o nome diferenciado do contêiner Partições.

Para obter mais informações e um exemplo de código que mostra esse método para localizar o contêiner Partitions, consulte a função **GetPartitionsDNSearch** em Código de Exemplo para Localizar o Contêiner [de Partições](example-code-for-locating-the-partitions-container.md).

O segundo método é mais fácil de implementar, mas se baseia no contêiner Partitions com um nome distinto relativo específico. No momento, não é possível alterar o nome do contêiner Partições, mas se essa funcionalidade for adicionada no futuro, o procedimento a seguir não funcionará corretamente se o contêiner Partições tiver sido renomeado.

1.  Agresse a RootDSE e obtenha o **atributo configurationNamingContext.**
2.  Combine a cadeia de caracteres "CN=Partitions", seguida pelo atributo **configurationNamingContext** para formar o nome diferenciado do contêiner Partitions. O nome diferenciado estará no formato "CN=Partitions,". <configuration DN>

Para obter mais informações e um exemplo de código que mostra esse método para localizar o contêiner Partitions, consulte a função **GetPartitionsDNManual** em Código de Exemplo para Localizar o Contêiner [de Partições](example-code-for-locating-the-partitions-container.md).

 

 