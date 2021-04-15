---
title: Criando uma partição de diretório de aplicativo
description: Uma partição de diretório de aplicativo é representada por um objeto domainDNS com um valor de atributo InstanceType de DS InstanceType, que o \_ \_ \_ \_ cabeçalho NC combinado com DS \_ InstanceType \_ NC \_ é \_ gravável.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Criando um AD de partição de diretório de aplicativo
- AD de partições de diretório de aplicativo, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17471696825179b6e49230b5168abbaf88b8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453941"
---
# <a name="creating-an-application-directory-partition"></a>Criando uma partição de diretório de aplicativo

Uma partição de diretório de aplicativo é representada por um objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) com um valor de atributo [**InstanceType**](/windows/desktop/ADSchema/a-instancetype) de **DS InstanceType, que o \_ \_ \_ \_ cabeçalho NC** combinado com **DS \_ InstanceType \_ NC \_ é \_ gravável**. Esse objeto **domainDns** representa a raiz da partição de diretório do aplicativo (cabeçalho NC) e é nomeado de forma semelhante a uma partição de domínio normal, por exemplo, "DC = DYNAMICDATA, DC = Fabrikam, DC = com", que corresponde a um nome DNS de "DynamicData.fabrikam.com". Uma partição de diretório de aplicativo pode, portanto, ser instanciada em qualquer lugar em que uma partição de domínio possa ser instanciada. Não há nenhum nome NetBIOS associado a uma partição de diretório de aplicativos.

É possível aninhar partições de diretório de aplicativo, ou seja, uma partição de diretório de aplicativo pode ter partições de diretório de aplicativo filho. Pesquisas com escopo de subárvore com raiz em um cabeçalho de partição de diretório de aplicativo gerarão referências de continuação para as partições de diretório de aplicativo filho.

Uma réplica de partição de diretório de aplicativo só pode ser criada em um controlador de domínio em execução no Windows Server 2003 e posterior e somente enquanto a função de Domain-Naming FSMO é mantida por um controlador de domínio do Windows Server 2003 e posterior. Em uma floresta mista que tem controladores de domínio do Windows Server 2003 e controladores de domínio de nível inferior (controladores de domínio do Windows 2000 ou controladores de domínio primários do Windows NT 4,0), uma tentativa de criar uma réplica de partição de diretório de aplicativo em um controlador de domínio de nível inferior falhará.

Uma partição de diretório de aplicativo também tem um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) correspondente no contêiner partições da partição de configuração. O **crossRef** pode ser criado previamente manualmente antes de criar o objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) . O objeto **crossRef** criado previamente deve ter os valores de atributo mostrados na tabela a seguir ou a criação da partição falhará. Se o objeto **crossRef** não existir, o servidor de Active Directory criará um quando a partição de diretório de aplicativo for criada.

| Atributo                          | Descrição                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contém o caminho DNS do controlador de domínio no qual a partição de diretório de aplicativo será criada.                               |
| [**habilitado**](/windows/desktop/ADSchema/a-enabled) | Contém **false**.                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Contém o nome distinto da partição. No exemplo acima, esse atributo conterá "DC = DynamicData, DC = mydomain, DC = com". |



 

**Para criar uma nova partição de diretório de aplicativo com sua primeira réplica, execute as seguintes etapas**

1.  Associe-se ao namespace da nova partição, especificando o controlador de domínio que hospedará a partição de diretório do aplicativo no ADsPath. Por exemplo, para criar uma partição com um ADsPath de "DC = DynamicData, DC = mydomain, DC = com", o ADsPath de ligação seria "LDAP:// <domain controller> /DC = mydomain, DC = com", em que " &lt; Domain Controller &gt; " é o nome DNS do controlador de domínio que hospedará a partição.

    A operação de associação deve especificar as opções de delegação e rápida. A opção rápida permite que a ligação seja realizada com sucesso mesmo que o namespace não exista. A opção de delegação é necessária para permitir que o controlador de domínio entre em contato com o detentor da função FSMO Domain-Naming usando as mesmas credenciais.

    A versão do sistema do controlador de domínio deve ser o sistema operacional Windows Server 2003 e posterior.

2.  Crie um objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) com um nome apropriado para a partição, por exemplo, "DC = DynamicData", para representar o cabeçalho de contexto de nomenclatura para a nova partição. O objeto **domainDns** deve ter um atributo [**InstanceType**](/windows/desktop/ADSchema/a-instancetype) com um valor de 5 (**DS \_ InstanceType \_ é o \_ NC \_** de instância DS de não \| **\_ \_ \_ pode ser \_ gravado**). O atributo **InstanceType** só pode ser definido no momento da criação porque é um atributo somente do sistema.

Quando o objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) for criado, o servidor de Active Directory executará as seguintes etapas:

1.  Pesquisa um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) no contêiner de partições que tem um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que corresponde ao nome distinto da partição e, se uma correspondência for encontrada, modifica o objeto **crossRef** para representar a partição de diretório do aplicativo. Se um objeto **crossRef** correspondente não for encontrado, o servidor de Active Directory criará um novo objeto **crossRef** para representar a partição de diretório do aplicativo.

    A tabela a seguir lista atributos importantes do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

    | Atributo                                                              | Descrição                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | Contém o nome distinto da partição.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contém o nome DNS da partição.                                                                                                            |
    | [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | O nome distinto do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) do controlador de domínio para a primeira réplica é adicionado a esse atributo. |

    

     

2.  Inicie uma sincronização da partição de configuração e aguarde a conclusão. Isso permite que o aplicativo cliente modifique parâmetros de configuração para a partição de diretório de aplicativo recém-criada enquanto estiver associado ao mesmo controlador de domínio usado para criar a partição de diretório de aplicativo.
3.  Crie o objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) com o **DS \_ InstanceType \_ \_ \_** , e o NC de **\_ instância DS \_ \_ não é \_** um sinalizador gravável definido na propriedade [**InstanceType**](/windows/desktop/ADSchema/a-instancetype) . A propriedade **InstanceType** também pode conter outros sinalizadores privados.
4.  Preencha o atributo [**MS-DS-tem-Master-NCS**](/windows/desktop/ADSchema/a-msds-hasmasterncs) do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para o controlador de domínio de destino com o nome distinto da partição de diretório de aplicativo recém-criada.

Quando a partição de diretório de aplicativo é criada ou quando uma nova réplica da partição de diretório de aplicativo é adicionada e totalmente sincronizada, o servidor de Active Directory registra corretamente a réplica com NetLogon e DNS. Para obter mais informações e uma lista dos registros SRV registrados, consulte [localizando um servidor de host de partição de diretório de aplicativo](locating-an-application-directory-partition-host-server.md).

Para obter mais informações sobre como criar uma partição de diretório de aplicativo, consulte [código de exemplo para criar uma partição de diretório de aplicativo](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Localizando o contêiner de partições

O nome distinto do contêiner de partições pode ser encontrado de uma das duas maneiras. A primeira é mais complicada de executar, mas sempre fornecerá um resultado preciso:

1.  Associe-se a RootDSE e obtenha o atributo **configurationNamingContext** .
2.  Use o atributo **configurationNamingContext** para associar ao contêiner de configuração.
3.  Pesquise no contêiner de configuração um objeto que seja do tipo [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) .
4.  Obtenha o valor do atributo **distinguishedName** do objeto [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) . Esse será o nome distinto do contêiner de partições.

Para obter mais informações e um exemplo de código que mostra esse método para localizar o contêiner de partições, consulte a função **GetPartitionsDNSearch** no [código de exemplo para localizar o contêiner de partições](example-code-for-locating-the-partitions-container.md).

O segundo método é mais fácil de implementar, mas depende do contêiner de partições com um nome distinto relativo específico. No momento, não é possível alterar o nome do contêiner de partições, mas se esse recurso for adicionado no futuro, o procedimento abaixo não funcionará corretamente se o contêiner de partições tiver sido renomeado.

1.  Associe-se a RootDSE e obtenha o atributo **configurationNamingContext** .
2.  Combine a cadeia de caracteres "CN = Partitions", seguido pelo atributo **configurationNamingContext** para formar o nome distinto do contêiner partições. O nome diferenciado estará no formato "CN = Partitions <configuration DN> ".

Para obter mais informações e um exemplo de código que mostra esse método para localizar o contêiner de partições, consulte a função **GetPartitionsDNManual** no [código de exemplo para localizar o contêiner de partições](example-code-for-locating-the-partitions-container.md).

 

 