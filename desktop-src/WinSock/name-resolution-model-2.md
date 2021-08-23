---
description: Um namespace refere-se a alguma funcionalidade para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis.
ms.assetid: 4139a8c2-d940-41e0-a3e8-fce3b70a1ff3
title: Modelo de resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23395cc6db5a93ec572f59e0d5ac6aaa7890c5c42a7966b86601eb190a54796
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822773"
---
# <a name="name-resolution-model"></a>Modelo de resolução de nomes

Um *namespace* refere-se a alguma funcionalidade para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis. Muitos namespaces estão atualmente em amplo uso, incluindo o DNS [(Sistema](../dns/dns-start-page.md) de Nomes de Domínio) da Internet, Active Directory Domain Services , [a](../ad/active-directory-domain-services.md)bindery, Serviços de diretório do NetWare (NDS) da Novell e X.500. Esses namespaces variam muito na forma como são organizados e implementados. Algumas de suas propriedades são particularmente importantes de entender da perspectiva da resolução de nomes winsock.

## <a name="types-of-namespaces"></a>Tipos de namespaces

Há três tipos diferentes de namespaces nos quais um serviço pode ser registrado:

-   Dinâmico
-   Estático
-   Persistente

Os namespaces dinâmicos permitem que os serviços se registrem com o namespace em tempo real e que os clientes descubram os serviços disponíveis em tempo de executar. Namespaces dinâmicos frequentemente dependem de difusões para indicar a disponibilidade contínua de um serviço de rede. Exemplos mais antigos de namespaces dinâmicos incluem o namespace SAP (Service Advertising Protocol) usado em um ambiente do NetWare e o namespace NBP (Name Binding Protocol) usado pelo AppleTalk. O namespace PNRP (Peer Name Resolution Protocol) usado Windows é um exemplo mais recente de um namespace dinâmico.

Os namespaces estáticos exigem que todos os serviços sejam registrados com antecedência, ou seja, quando o namespace é criado. Um exemplo de namespace estático são os *hosts*, *protocolo* e arquivos *de* serviços usados pela maioria das implementações de TCP/IP. No Windows, esses arquivos normalmente estão localizados na *pasta C: \\ drivers do windows \\ system32 \\ \\ etc.*

Namespaces persistentes permitem que os serviços se registrem com o namespace em tempo real. No entanto, ao contrário dos namespaces dinâmicos, os namespaces persistentes retêm as informações de registro no armazenamento nãovolatile em que permanecem até o momento em que o serviço solicita que sejam removidos. Namespaces persistentes são tipados por serviços de diretório, como X.500 e NDS (Serviço de Diretório do NetWare). Esses ambientes permitem a adição, exclusão e modificação de propriedades de serviço. Além disso, o objeto de serviço que representa o serviço no serviço de diretório pode ter uma variedade de atributos associados ao serviço. O atributo mais importante para aplicativos cliente são as informações de endereçamento do serviço. DNS é outro exemplo de um namespace persistente. Embora haja uma maneira programática de resolver nomes DNS usando soquetes Windows, o provedor de namespace DNS no Windows não dá suporte ao registro de novos nomes DNS usando Winsock. Você deve usar as funções DNS diretamente para registrar nomes DNS. Para obter mais informações, consulte a [Referência de DNS.](../dns/dns-reference.md)

## <a name="namespace-organization"></a>Organização do namespace

Muitos namespaces são organizados hierarquicamente. Alguns, como X.500 e NDS, permitem aninhamento ilimitado. Outros permitem que os serviços sejam combinados em um único nível de hierarquia ou grupo. Normalmente, isso é conhecido como um *grupo de trabalho*. Ao construir uma consulta, geralmente é necessário estabelecer um ponto de contexto dentro de uma hierarquia de namespace na qual a pesquisa será iniciada.

## <a name="namespace-provider-architecture"></a>Arquitetura do provedor de namespace

Naturalmente, as interfaces programáticas usadas para consultar os vários tipos de namespaces e registrar informações em um namespace (se há suporte) diferem amplamente. Um provedor de *namespace* é um software residente localmente que sabe como mapear entre a SPI do namespace winsock e algum namespace existente (que pode ser implementado localmente ou acessado por meio da rede). A arquitetura do provedor de namespace é ilustrada da seguinte forma:

![arquitetura do provedor de namespace](images/ovrvw3-1.png)

Observe que é possível que um determinado namespace, digamos DNS, tenha mais de um provedor de namespace instalado em um determinado computador.

Conforme mencionado acima, o serviço de termo *genérico* refere-se à metade do servidor de um aplicativo cliente/servidor. No Winsock, um serviço é associado *a* uma classe de serviço  e cada instância de um serviço específico tem um nome de serviço que deve ser exclusivo dentro da classe de serviço. Exemplos de classes de serviço incluem Servidor FTP, SQL Server, XYZ Corp. Employee Info Server etc. Como o exemplo tenta ilustrar, algumas classes de serviço são bem conhecidas, enquanto outras são exclusivas e específicas para um aplicativo vertical específico. Em ambos os casos, cada classe de serviço é representada por um nome de classe e um identificador de classe. O nome da classe não precisa necessariamente ser exclusivo, mas o identificador de classe deve ser. GuiDs (Identificadores Globalmente Exclusivos) são usados para representar identificadores de classe de serviço. Para serviços conhecidos, nomes de classe e GUIDs (identificadores de classe) foram pré-alocados e macros estão disponíveis para conversão entre, por exemplo, números de porta TCP (na ordem de byte do host) e os GUIDs de identificador de classe correspondentes. Para outros serviços, o desenvolvedor escolhe o nome da classe e usa o utilitário Uuidgen.exe para gerar um GUID para o identificador de classe.

A noção de uma classe de serviço existe para permitir que um conjunto de atributos seja estabelecido que são mantidos em comum por todas as instâncias de um serviço específico. Esse conjunto de atributos é fornecido no momento em que a classe de serviço é definida como Winsock e é conhecida como as informações de esquema da classe de serviço. Quando um serviço é instalado e disponibilizado em um computador host, esse serviço é considerado instanciado e seu nome de serviço é usado para distinguir uma instância específica do serviço de outras instâncias que podem ser conhecidas pelo namespace .

Observe que a instalação de uma classe de serviço só precisa ocorrer em computadores em que o serviço é executado, não em todos os clientes que podem utilizar o serviço. Sempre que possível, o Ws232.dll fornece informações de esquema de classe de serviço para um provedor de namespace no momento em que uma instanação de um serviço deve ser registrada ou uma consulta de serviço é \_ iniciada. O Ws232.dll, é claro, armazena essas informações em si, mas tenta recuperá-las de um provedor de namespace que indicou sua capacidade de fornecer \_ esses dados. Como não há nenhuma garantia de que o Ws232.dll possa fornecer o esquema de classe de serviço, os provedores de namespace que precisam dessa informação devem ter um mecanismo de fallback para obter isso por meio de meios específicos do \_ namespace.

Conforme mencionado acima, a Internet adota o que pode ser conhecido como um modelo de serviço centrado em host. Os aplicativos que precisam localizar o endereço de transporte de um serviço geralmente devem primeiro resolver o endereço de um host específico conhecido para hospedar o serviço. Para esse endereço, eles adicionam o número da porta conhecido e, portanto, criam um endereço de transporte completo. Para facilitar a resolução de nomes de host, um identificador de classe de serviço especial foi pré-alocado (**SVCID \_ HOSTNAME**). Uma consulta que especifica **SVCID \_ HOSTNAME** como a classe de serviço e especifica um nome de host para o nome da instância de serviço retornará informações de endereço do host se a consulta for bem-sucedida.

No Windows Soquetes 2, os aplicativos que são independentes de protocolo devem evitar a necessidade de compreender os detalhes internos de um endereço de transporte. Portanto, a necessidade de primeiro obter um endereço de host e, em seguida, adicionar na porta é problemática. Para evitar isso, as consultas também podem incluir o nome conhecido de um serviço específico e o protocolo sobre o qual o serviço opera, como FTP sobre TCP. Nesse caso, uma consulta bem-sucedida retorna um endereço de transporte completo para o serviço especificado no host indicado e o aplicativo não é necessário para inspecionar os internos de uma estrutura [**sockaddr.**](sockaddr-2.md)

O Sistema de Nomes de Domínio da Internet não tem um meio bem definido para armazenar informações de esquema de classe de serviço. Como resultado, os provedores de namespace dns para Winsock só podem acomodar serviços TCP/IP conhecidos para os quais um GUID de classe de serviço foi pré-alocado.

Na prática, essa não é uma limitação grave, pois os GUIDs de classe de serviço foram pré-alocados para todo o conjunto de portas TCP e UDP e macros estão disponíveis para recuperar o GUID associado a qualquer porta TCP ou UDP com a porta expressa na ordem de byte do host. Portanto, todos os serviços familiares, como HTTP, FTP, Telnet, Whois etc. são bem suportados.

Continuando com nosso exemplo de classe de serviço, os nomes de instância do serviço FTP podem ser "alder.intel.com" ou "ftp.microsoft.com", enquanto uma instância do XYZ Corp. Employee Info Server pode ser nomeada "XYZ Corp. Employee Info Server Version 3.5".

Nos dois primeiros casos, a combinação do GUID da classe de serviço para FTP e o nome do computador (fornecido como o nome da instância de serviço) identificam exclusivamente o serviço desejado. No terceiro caso, o nome do host em que o serviço reside pode ser descoberto no momento da consulta de serviço, portanto, o nome da instância de serviço não precisa incluir um nome de host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de DNS](../dns/dns-reference.md)
</dt> <dt>

[Estruturas de dados de resolução de nomes](name-resolution-data-structures-2.md)
</dt> <dt>

[Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nomes](registration-and-name-resolution-2.md)
</dt> <dt>

[**Sockaddr**](sockaddr-2.md)
</dt> <dt>

[Resumo das funções de resolução de nomes](summary-of-name-resolution-functions-2.md)
</dt> </dl>

 

 
