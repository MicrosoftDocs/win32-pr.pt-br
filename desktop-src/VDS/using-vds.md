---
description: Usando VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: Usando VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c648c5cc2507c4819f98367c367099248a0e723f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171662"
---
# <a name="using-vds"></a>Usando VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O VDS fornece uma interface para o desenvolvimento de scripts e GUI que pode simplificar as atividades executadas por um administrador do Windows Server que gerencia um conjunto heterogêneo de sistemas de armazenamento, migrando dados entre diferentes configurações de hardware ao longo do tempo. Se você não estiver familiarizado com os objetos que são usados no desenvolvimento do VDS, consulte o [modelo de objeto do VDS](vds-object-model.md).

Alguns pontos antes de começar:

-   Embora o VDS inclua um provedor de software, você deve adquirir um provedor de hardware e o hardware associado separadamente para tirar proveito das operações do provedor de hardware. Para obter instruções de instalação, consulte a documentação fornecida pelo fabricante do hardware.
-   Algumas operações exigem volumes formatados com NTFS. Por exemplo, quando você monta um volume em um diretório existente, o volume que contém o diretório deve ser formatado com NTFS. Outros sistemas de arquivos não oferecem suporte a essa operação. Para obter informações sobre as operações que exigem NTFS, consulte cada página de método na [referência do VDS](vds-reference.md).

## <a name="programming-languages"></a>Linguagens de programação

Use qualquer linguagem de programação adequada para desenvolvimento com com, como a linguagem C ou C++.

## <a name="security"></a>Segurança

O Firewall do Windows está habilitado por padrão. Isso pode fazer com que a autenticação falhe para interfaces de retorno de chamada, como [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink), que pode ser executada remotamente. Se o Firewall do Windows estiver habilitado no cliente ou no servidor, você deverá adicionar o gerenciamento de volume remoto à guia **exceções** no firewall do Windows.

**Windows Server 2003:** No Windows Server 2003 com Service Pack 2 (SP2) e Windows Server 2003 com Service Pack 1 (SP1), se o Firewall do Windows estiver habilitado no cliente ou no servidor e se o servidor estiver configurado para usar a autenticação NTLM, você deverá adicionar as seguintes configurações à guia **exceções** no firewall do Windows para o computador apropriado.

| Computador                 | Configurações de exceções                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
| Computador cliente (local)  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
| Computador servidor (remoto) | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

Observe que o Firewall do Windows não está habilitado por padrão até o Windows Server 2003 com SP1.

Um aplicativo que está usando o VDS deve ser executado sob a conta de grupo de operadores de backup ou administradores. Sem o privilégio apropriado, um aplicativo pode criar um objeto de carregador de serviço, mas o objeto não carregará o VDS. Em vez disso, ele retorna um erro indicando que o acesso ao VDS foi negado.

Se a rede usar a autenticação NTLM, o computador cliente deverá permitir o acesso anônimo. Nesse caso, se o computador cliente estiver executando um sistema operacional Windows Server, o acesso anônimo será habilitado por padrão. Se estiver executando um sistema operacional cliente Windows, o acesso anônimo deverá ser habilitado usando Dcomcnfg.exe.

## <a name="configuration-and-query-operations"></a>Operações de configuração e consulta

As operações de configuração e consulta têm como escopo o computador, o provedor, o subsistema ou o pacote mais relevante. As consultas atravessam apenas um provedor ou um nível da hierarquia de associação. Para criar uma exibição completa, o chamador deve fazer uma consulta horizontal e verticalmente em cada nível. A lista a seguir inclui exemplos:

-   Para exibir todos os discos em um computador, os chamadores devem consultar todos os provedores de software para os discos que são reivindicados por esses provedores.
-   Para determinar quais discos contribuem para um volume empilhado por software, os chamadores primeiro determinam os plexes contribuintes e, em seguida, consultam as extensões de disco para cada Plex.
-   Para exibir todas as unidades que estão anexadas a um determinado subsistema, os chamadores devem consultar o subsistema.
-   Para exibir todos os LUNs expostos por um determinado subsistema, os chamadores devem consultar o subsistema.
-   Para exibir todo o armazenamento em uma SAN ou em um cluster, os chamadores devem consultar cada computador para todos os provedores de hardware, consultar cada provedor de todos os subsistemas e, em seguida, consultar cada subsistema.

Embora cada consulta individual não retorne duplicatas, as consultas repetidas entre computadores ou entre provedores podem acumular duplicatas. Os chamadores devem implementar qualquer filtragem. Observe também que os aplicativos de gerenciamento de SAN podem usar o Active Directory ou um repositório para manter as informações de configuração; Talvez não seja necessário consultar cada computador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviço de Disco Virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objeto VDS](vds-object-model.md)
</dt> <dt>

[Referência do VDS](vds-reference.md)
</dt> </dl>

 

