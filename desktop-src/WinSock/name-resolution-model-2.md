---
description: Um namespace refere-se a algum recurso para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modelo de resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb209254dcee2419e1ed92c017fc7d37dc9c0a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501688"
---
# <a name="name-resolution-model"></a>Modelo de resolução de nomes

Um *namespace* refere-se a algum recurso para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis. Muitos namespaces estão atualmente em uso amplo, incluindo o DNS ( [sistema de nomes de domínio](../dns/dns-start-page.md) ) da Internet, [Active Directory Domain Services](../ad/active-directory-domain-services.md), a ligação, serviços de diretório do NetWare (NDS) da Novell e X. 500. Esses namespaces variam muito em como são organizados e implementados. Algumas de suas propriedades são particularmente importantes para entender a partir da perspectiva da resolução de nomes do Winsock.

## <a name="types-of-namespaces"></a>Tipos de namespaces

Há três tipos diferentes de namespaces nos quais um serviço pode ser registrado:

-   Dinâmico
-   Estático
-   Persistente

Os namespaces dinâmicos permitem que os serviços se registrem com o namespace dinamicamente e para que os clientes descubram os serviços disponíveis em tempo de execução. Os namespaces dinâmicos frequentemente dependem de difusões para indicar a disponibilidade contínua de um serviço de rede. Exemplos mais antigos de namespaces dinâmicos incluem o namespace SAP (Service Advertising Protocol) usado em um ambiente do NetWare e o namespace NBP (protocolo de ligação de nome) usado pelo AppleTalk. O Namespace PNRP (Peer Name Resolution Protocol) usado no Windows é um exemplo mais recente de um namespace dinâmico.

Os namespaces estáticos exigem que todos os serviços sejam registrados antecipadamente, ou seja, quando o namespace é criado. Um exemplo de um namespace estático são os arquivos *hosts*, *protocolo* e *Serviços* usados pela maioria das implementações de TCP/IP. No Windows, esses arquivos normalmente estão localizados na pasta *C: \\ Windows \\ System32 \\ drivers \\ etc* .

Namespaces persistentes permitem que os serviços se registrem com o namespace em tempo real. Ao contrário dos namespaces dinâmicos, no entanto, os namespaces persistentes retêm as informações de registro no armazenamento não volátil onde permanecem até o momento em que as solicitações de serviço são removidas. Os namespaces persistentes são Typified por serviços de diretório, como X. 500 e o NDS (serviço de diretório do NetWare). Esses ambientes permitem a adição, exclusão e modificação de propriedades de serviço. Além disso, o objeto de serviço que representa o serviço no serviço de diretório pode ter uma variedade de atributos associados ao serviço. O atributo mais importante para aplicativos cliente são as informações de endereçamento do serviço. O DNS é outro exemplo de um namespace persistente. Embora haja uma maneira programática de resolver nomes DNS usando o Windows Sockets, o provedor de namespace DNS no Windows não dá suporte ao registro de novos nomes DNS usando o Winsock. Você deve usar as funções de DNS diretamente para registrar nomes DNS. Para obter mais informações, consulte a [referência de DNS](../dns/dns-reference.md).

## <a name="namespace-organization"></a>Organização de namespace

Muitos namespaces são organizados hierarquicamente. Alguns, como X. 500 e NDS, permitem aninhamento ilimitado. Outros permitem que os serviços sejam combinados em um único nível de hierarquia ou grupo. Isso é normalmente chamado de grupo de *trabalho*. Ao construir uma consulta, geralmente é necessário estabelecer um ponto de contexto dentro de uma hierarquia de namespace da qual a pesquisa será iniciada.

## <a name="namespace-provider-architecture"></a>Arquitetura do provedor de namespace

Naturalmente, as interfaces programáticas usadas para consultar os vários tipos de namespaces e registrar informações em um namespace (se houver suporte) diferem muito. Um *provedor de namespace* é uma parte do software residente localmente que sabe como mapear entre o SPI do namespace do Winsock e algum namespace existente (que poderia ser implementado localmente ou ser acessado pela rede). A arquitetura do provedor de namespace é ilustrada da seguinte maneira:

![arquitetura do provedor de namespace](images/ovrvw3-1.png)

Observe que é possível que um determinado namespace, digamos, o DNS, tenha mais de um provedor de namespace instalado em um determinado computador.

Conforme mencionado acima, o termo genérico *serviço* se refere à metade do servidor de um aplicativo cliente/servidor. No Winsock, um serviço é associado a uma *classe de serviço*, e cada instância de um serviço específico tem um *nome de serviço* que deve ser exclusivo dentro da classe de serviço. Exemplos de classes de serviço incluem servidor FTP, SQL Server, XYZ Corp. servidor de informações de funcionários, etc. Como o exemplo tenta ilustrar, algumas classes de serviço são bem conhecidas, enquanto outras são exclusivas e específicas para um aplicativo vertical específico. Em ambos os casos, cada classe de serviço é representada por um nome de classe e um identificador de classe. O nome da classe não precisa necessariamente ser exclusivo, mas o identificador de classe deve ser. Os GUIDs (identificadores globalmente exclusivos) são usados para representar identificadores de classe de serviço. Para serviços conhecidos, os nomes de classe e os GUIDs (identificadores de classe) foram alocados previamente e as macros estão disponíveis para conversão entre, por exemplo, números de porta TCP (na ordem de bytes de host) e os GUIDs de identificador de classe correspondentes. Para outros serviços, o desenvolvedor escolhe o nome da classe e usa o utilitário Uuidgen.exe para gerar um GUID para o identificador de classe.

A noção de uma classe de serviço existe para permitir que um conjunto de atributos seja estabelecido e que seja mantido em comum por todas as instâncias de um serviço específico. Esse conjunto de atributos é fornecido no momento em que a classe de serviço é definida como Winsock e é chamada de informações de esquema de classe de serviço. Quando um serviço é instalado e disponibilizado em um computador host, esse serviço é considerado *instanciado* e seu nome de serviço é usado para distinguir uma instância específica do serviço de outras instâncias que podem ser conhecidas pelo namespace.

Observe que a instalação de uma classe de serviço só precisa ocorrer em computadores em que o serviço é executado, e não em todos os clientes que podem utilizar o serviço. Sempre que possível, o \_32.dll Ws2 fornece informações de esquema de classe de serviço para um provedor de namespace no momento em que uma instanciação de um serviço é registrada ou uma consulta de serviço é iniciada. O \_32.dll Ws2 não, é claro, armazenar essas informações em si, mas tenta recuperá-las de um provedor de namespace que indicou sua capacidade de fornecer esses dados. Como não há nenhuma garantia de que o \_32.dll Ws2 possa fornecer o esquema de classe de serviço, os provedores de namespace que precisam dessas informações devem ter um mecanismo de fallback para obtê-lo por meio de meios específicos de namespace.

Conforme observado acima, a Internet adotou o que pode ser chamado de um modelo de serviço centrado em host. Os aplicativos que precisam localizar o endereço de transporte de um serviço geralmente devem primeiro resolver o endereço de um host específico conhecido para hospedar o serviço. Para esse endereço, eles adicionam o número da porta conhecida e, portanto, criam um endereço de transporte completo. Para facilitar a resolução de nomes de host, um identificador de classe de serviço especial foi pré-alocado **( \_ nome de host SVCID**). Uma consulta que especifica o nome de host **SVCID \_** como a classe de serviço e especifica que um nome de host para a instância de serviço retornará informações de endereço de host se a consulta for bem-sucedida.

No Windows Sockets 2, os aplicativos que são independentes de protocolo devem evitar a necessidade de compreender os detalhes internos de um endereço de transporte. Portanto, a necessidade de obter primeiro um endereço de host e, em seguida, adicionar na porta é problemática. Para evitar isso, as consultas também podem incluir o nome conhecido de um serviço específico e o protocolo sobre o qual o serviço opera, como o FTP sobre TCP. Nesse caso, uma consulta bem-sucedida retorna um endereço de transporte completo para o serviço especificado no host indicado e o aplicativo não é necessário para inspecionar os elementos internos de uma estrutura [**SOCKADDR**](sockaddr-2.md) .

O sistema de nomes de domínio da Internet não tem um meio bem definido para armazenar informações de esquema de classe de serviço. Como resultado, os provedores de namespace DNS para Winsock podem acomodar apenas os serviços TCP/IP conhecidos para os quais um GUID de classe de serviço foi alocado previamente.

Na prática, essa não é uma limitação séria, pois os GUIDs de classe de serviço foram alocados previamente para todo o conjunto de portas TCP e UDP, e as macros estão disponíveis para recuperar o GUID associado a qualquer porta TCP ou UDP com a porta expressa na ordem de bytes de host. Assim, todos os serviços familiares, como HTTP, FTP, Telnet, Whois etc., têm suporte.

Continuando com nosso exemplo de classe de serviço, os nomes de instância do serviço FTP podem ser "alder.intel.com" ou "ftp.microsoft.com", enquanto uma instância do servidor de informações do funcionário XYZ pode ser denominada "XYZ Corp. Employee info Server versão 3,5".

Nos dois primeiros casos, a combinação do GUID de classe de serviço para FTP e o nome do computador (fornecido como o nome da instância de serviço) identifica exclusivamente o serviço desejado. No terceiro caso, o nome do host em que o serviço reside pode ser descoberto no momento da consulta de serviço, portanto, o nome da instância do serviço não precisa incluir um nome de host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de DNS](../dns/dns-reference.md)
</dt> <dt>

[Estruturas de dados de resolução de nomes](name-resolution-data-structures-2.md)
</dt> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Resumo das funções de resolução de nomes](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
