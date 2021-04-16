---
description: O WMI fornece uma interface uniforme para quaisquer aplicativos ou scripts locais ou remotos que obtêm dados de gerenciamento de um sistema de computador, rede ou empresa.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Arquitetura do WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562275"
---
# <a name="wmi-architecture"></a>Arquitetura do WMI

O WMI fornece uma interface uniforme para quaisquer aplicativos ou scripts locais ou remotos que obtêm dados de gerenciamento de um sistema de computador, rede ou empresa. A interface uniforme foi projetada de modo que os scripts e aplicativos cliente WMI não precisem chamar uma ampla variedade de interfaces de programação de aplicativo (APIs) do sistema operacional. Muitas APIs não podem ser chamadas por clientes de automação, como scripts ou aplicativos Visual Basic. Outras APIs não fazem chamadas para computadores remotos.

Para obter dados do WMI, grave um script de cliente ou aplicativo que acesse as [classes WMI](wmi-classes.md) ou forneça dados para o WMI escrevendo um [*provedor WMI*](gloss-p.md). Para obter mais informações, consulte [usando o WMI](using-wmi.md).

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objetos, consumidores e infraestrutura do WMI

O diagrama a seguir mostra a relação entre a infraestrutura do WMI e os provedores do WMI e os objetos gerenciados e também mostra a relação entre a infraestrutura do WMI e os consumidores do WMI.

![relação entre a infraestrutura do WMI, os provedores de WMI e os objetos gerenciados](images/wmi-architecture.png)

## <a name="wmi-components"></a>Componentes WMI

A lista a seguir descreve os principais componentes WMI:

-   Objetos gerenciados e provedores de WMI

    Um provedor WMI é um objeto COM que monitora um ou mais [*objetos gerenciados*](gloss-m.md) para o WMI. Um objeto gerenciado é um componente corporativo lógico ou físico, como uma unidade de disco rígido, adaptador de rede, sistema de banco de dados, sistema operacional, processo ou serviço.

    Semelhante a um driver, um provedor fornece o WMI com dados de um objeto gerenciado e manipula mensagens do WMI para o objeto gerenciado. Os provedores WMI consistem em um arquivo DLL e um arquivo [*MOF (formato MOF)*](gloss-m.md) que define as classes para as quais o provedor retorna dados e executa operações. Provedores, como aplicativos WMI C++, usam a [API com para o WMI](com-api-for-wmi.md). Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).

    Um exemplo de provedor é o [provedor de registro](/previous-versions/windows/desktop/regprov/system-registry-provider)pré-instalado, que acessa os dados no registro do sistema. O provedor de registro tem uma [*classe WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), com muitos métodos, mas sem propriedades. Outros provedores pré-instalados, como o [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider), normalmente têm classes com muitas propriedades, mas poucos métodos, como o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou o disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). O arquivo DLL do provedor de registro, Stdprov.dll, contém o código que retorna dados dinamicamente quando solicitado por scripts ou aplicativos cliente.

    Os arquivos MOF e DLL WMI estão localizados em% WINDIR% \\ System32 \\ WBEM, juntamente com as [ferramentas de Command-Line WMI](wmi-command-line-tools.md), como [**Winmgmt.exe**](winmgmt.md) e [**Mofcomp.exe**](mofcomp.md). As classes de provedor, como o [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), são definidas em arquivos MOF e, em seguida, compiladas no repositório WMI na inicialização do sistema.

-   [Infraestrutura WMI](wmi-infrastructure.md)

    A infraestrutura do WMI é um componente do sistema operacional Microsoft Windows conhecido como o serviço WMI (Winmgmt). A infraestrutura do WMI tem dois componentes: o núcleo do WMI e o [*repositório do WMI*](gloss-w.md).

    O repositório WMI é organizado por [*namespaces*](gloss-n.md)WMI. O serviço WMI cria alguns namespaces como raiz \\ padrão, cimv2 raiz \\ e \\ assinatura raiz na inicialização do sistema e desinstala um conjunto padrão de definições de classe, incluindo as [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider), as classes de [sistema WMI](wmi-system-classes.md)e outras. Os namespaces restantes encontrados no sistema são criados por provedores para outras partes do sistema operacional ou produtos. Para obter mais informações e uma lista de provedores de WMI encontrados na maioria das versões do sistema operacional, consulte [provedores WMI](wmi-providers.md).

    O serviço WMI atua como um intermediário entre os provedores, os aplicativos de gerenciamento e o repositório do WMI. Somente dados estáticos sobre objetos são armazenados no repositório, como as classes definidas pelos provedores. O WMI Obtém a maioria dos dados dinamicamente do provedor quando um cliente o solicita. Você também pode configurar assinaturas para receber notificações de eventos de um provedor. Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).

-   Consumidores do WMI

    Um consumidor do WMI é um aplicativo de gerenciamento ou script que interage com a infraestrutura do WMI. Um aplicativo de gerenciamento pode consultar, enumerar dados, executar métodos de provedor ou assinar eventos chamando a [API com para WMI](com-api-for-wmi.md) ou a [API de script para WMI](scripting-api-for-wmi.md). Os únicos dados ou ações disponíveis para um objeto gerenciado, como uma unidade de disco ou um serviço, são aqueles que um provedor fornece.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> <dt>

[Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Fornecendo dados ao WMI](providing-data-to-wmi.md)
</dt> <dt>

[Classes WMI](wmi-classes.md)
</dt> <dt>

[Eventos de monitoramento](monitoring-events.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
