---
description: Interfaces programáticas usadas para consultar os vários tipos de namespaces e registrar informações em um namespace, se houver suporte, diferem muito.
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Arquitetura do provedor de namespace no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb567933cae60f56137eba39845bf27ad8c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164464"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Arquitetura do provedor de namespace no SPI

Interfaces programáticas usadas para consultar os vários tipos de namespaces e registrar informações em um namespace, se houver suporte, diferem muito. Um provedor de namespace é um aplicativo residente localmente que pode ser mapeado entre o SPI do namespace do Windows Sockets e um namespace existente que poderia ser implementado localmente ou acessado pela rede. Isso é ilustrado da seguinte maneira:

![diagrama do provedor de namespace](images/ovrvw3-1.png)

> [!Note]  
> É possível que um namespace específico, por exemplo, o DNS, tenha mais de um provedor de namespace instalado em um determinado computador.

 

Conforme mencionado acima, o termo genérico, serviço, refere-se à metade do servidor de um aplicativo cliente/servidor. No Windows Sockets, um serviço é associado a uma classe de serviço e cada instância de um serviço específico tem um nome de serviço que deve ser exclusivo dentro da classe de serviço. Exemplos de classes de serviço incluem servidor FTP, SQL Server, XYZ Corp. servidor de informações de funcionário e assim por diante.

Como o exemplo tenta ilustrar, algumas classes de serviço são bem conhecidas, enquanto outras são exclusivas e específicas para um aplicativo vertical específico. Em ambos os casos, cada classe de serviço é representada por um nome de classe e um identificador de classe. O nome da classe não precisa necessariamente ser exclusivo, mas o identificador de classe deve ser. Os GUIDs (identificadores globalmente exclusivos) são usados para representar IDs de classe de serviço. Para serviços conhecidos, nomes de classe e identificadores de classe (GUIDs) foram alocados e macros estão disponíveis para conversão entre, por exemplo, números de porta TCP e os GUIDs de identificador de classe correspondentes. Para outros serviços, o desenvolvedor escolhe o nome da classe e usa o utilitário Uuidgen.exe para gerar um GUID para o identificador de classe.

O conceito de uma classe de serviço existe para permitir que um conjunto de atributos seja estabelecido e que seja mantido em comum por todas as instâncias de um serviço específico. Esse conjunto de atributos é fornecido ao Windows Sockets no momento em que a classe de serviço é definida e é conhecida como informações de esquema de classe de serviço. O32.dll Ws2, por \_ sua vez, retransmite essas informações para todos os provedores de namespace ativos. Quando uma instância de um serviço é instalada e disponibilizada em um computador host, seu nome de serviço é usado para distinguir essa instância específica de outras que podem ser conhecidas pelo namespace.

Lembre-se de que a instalação de uma classe de serviço só precisa ocorrer em computadores em que o serviço é executado, não em todos os clientes que podem utilizar o serviço. Quando possível, a \_32.dll Ws2 fornecerá informações de esquema de classe de serviço para um provedor de namespace no momento em que uma instância de um serviço deve ser registrada ou uma consulta de serviço for iniciada. O \_32.dll Ws2 não, é claro, armazenar essas informações em si, mas tenta recuperá-las de um provedor de namespace que indicou sua capacidade de fornecer esses dados. Como não há nenhuma garantia de que o \_32.dll Ws2 será capaz de fornecer o esquema de classe de serviço, os provedores de namespace que exigem essas informações devem ter um mecanismo de fallback para obtê-lo por meio de meios específicos de namespace.

O sistema de nomes de domínio da Internet não tem um meio bem definido para armazenar informações de esquema de classe de serviço. Como resultado, os provedores de namespace DNS só poderão acomodar serviços TCP/IP conhecidos para os quais um GUID de classe de serviço tenha sido alocado previamente. Na prática, essa não é uma limitação séria, pois os GUIDs de classe de serviço foram alocados previamente para todo o conjunto de portas TCP e UDP, e as macros estão disponíveis para recuperar o GUID associado a qualquer porta TCP ou UDP. Assim, todos os serviços familiares, como FTP, Telnet, Whois etc., têm suporte. Ao consultar esses serviços, por convenção, o nome do host do computador de destino é o nome da instância de serviço.

Continuando com nosso exemplo de classe de serviço, os nomes de instância do serviço FTP podem ser "alder.intel.com" ou "rhino.microsoft.com", enquanto uma instância do servidor de informações do funcionário XYZ pode ser denominada "XYZ Corp. Employee info Server versão 3,5". Nos dois primeiros casos, a combinação do GUID de classe de serviço para FTP e o nome do computador (fornecido como o nome da instância de serviço) identifica exclusivamente o serviço desejado. No terceiro caso, o nome do host em que o serviço reside pode ser descoberto no momento da consulta de serviço, portanto, o nome da instância do serviço não precisa incluir um nome de host.

 

 



