---
description: A WMI (Instrumentação de Gerenciamento do Windows) é a implementação do WBEM (Gerenciamento Corporativo Baseado na Web) da Microsoft, que é uma iniciativa de mercado para desenvolver uma tecnologia padrão para acessar informações de gerenciamento em um ambiente corporativo.
ms.assetid: d745cf25-a139-439d-9ac5-e7720b640516
ms.tgt_platform: multiple
title: Sobre o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cf42ead6c3ae1b364ab8f83c83a744afa28734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297332"
---
# <a name="about-wmi"></a>Sobre o WMI

A WMI (Instrumentação de Gerenciamento do Windows) é a implementação do WBEM (Gerenciamento Corporativo Baseado na Web) da Microsoft, que é uma iniciativa de mercado para desenvolver uma tecnologia padrão para acessar informações de gerenciamento em um ambiente corporativo. A WMI usa o padrão de mercado CIM (Modelo de Informação Comum) para representar sistemas, aplicativos, redes, dispositivos e outros componentes gerenciados. O CIM é desenvolvido e mantido pela[DMTF](https://www.dmtf.org/standards/wsman)(Distributed Management Task Force).

> [!Note]  
> A próxima geração do WMI, conhecida como a MI (infraestrutura de gerenciamento do Windows), está disponível no momento. MI é totalmente compatível com as versões anteriores do WMI e fornece um host de recursos e benefícios que facilitam ainda mais o projeto e o desenvolvimento de provedores e clientes. Por exemplo, muitos provedores mais recentes são escritos usando a estrutura MI, mas podem ser acessados usando scripts e aplicativos WMI. Para obter mais informações sobre as diferenças entre as duas tecnologias, consulte [por que usar mi?](/previous-versions/windows/desktop/wmi_v2/why-use-mi-)

 

## <a name="managing-remote-computer-systems-with-wmi"></a>Gerenciando sistemas de computador remoto com o WMI

A capacidade de obter dados de gerenciamento de computadores remotos é o que torna a WMI útil. As conexões WMI remotas são estabelecidas por meio do DCOM. Uma alternativa é usar Gerenciamento Remoto do Windows ([WinRM](/windows/desktop/WinRM/portal)), que obtém dados remotos de gerenciamento de WMI usando o protocolo baseado em SOAP WS-Management.

## <a name="programming-with-wmi"></a>Programando com o WMI

Aplicativos de gerenciamento ou scripts podem obter dados ou executar operações por meio do WMI em uma variedade de idiomas. Para obter mais informações, consulte a seção público do desenvolvedor em [Instrumentação de gerenciamento do Windows](wmi-start-page.md).

Muitos recursos do Windows têm provedores WMI associados, como o [provedor de dados de configuração da inicialização (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) ou o [provedor de volume de armazenamento](/previous-versions/windows/desktop/vdswmi/storage-volume-provider). Os provedores WMI implementam a funcionalidade descrita por métodos e propriedades de classes WMI para gerenciar recursos do Windows associados. Para obter mais informações, consulte [provedores WMI](wmi-providers.md) e [classes WMI](wmi-classes.md).

Para obter mais informações sobre como escrever um provedor para fornecer dados de novos hardwares ou aplicativos, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).

Para obter mais informações sobre como implementar essa tecnologia, consulte [usando o WMI](using-wmi.md).

A tabela a seguir lista os tópicos incluídos nesta seção.



| Seção                                                                                                | Descrição                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [O que há de novo no WMI](what-s-new-in-wmi.md)                                                             | Novos recursos no WMI.                                                                                                                                                                                                                              |
| [Disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md) | Alguns componentes não estão mais disponíveis ou estão disponíveis como uma instalação opcional.                                                                                                                                                             |
| [Arquitetura do WMI](wmi-architecture.md)                                                               | Um aplicativo de gerenciamento se comunica com o WMI usando uma variedade de interfaces, como Visual Basic, C++, ODBC e ActiveX. Todas as interfaces WMI são baseadas na Component Object Model (COM).                                              |
| [Modelo CIM](common-information-model.md)                                               | Um modelo de programação independente de linguagem que usa técnicas orientadas a objeto para descrever uma empresa.                                                                                                                                          |
| [Managed Object Format](managed-object-format--mof-.md)                                               | Um formato que permite criar código legível, que o sistema operacional pode converter em um conjunto de classes CIM. Você pode usar as novas classes para modelar e controlar novas tecnologias para uma empresa.                                 |
| [Controle de conta de usuário e WMI](user-account-control-and-wmi.md)                                       | O UAC (controle de conta de usuário) afeta quais dados do WMI são retornados, acesso remoto e como os scripts devem ser executados. Para obter mais informações, consulte [introdução com o controle de conta de usuário no Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista). |
| [Acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md)                                 | O WMI usa os objetos e procedimentos de segurança padrão do Windows para controlar e proteger o acesso a objetos protegíveis, como namespaces, impressoras, serviços e aplicativos DCOM do WMI.                                                                      |
| [Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)                                     | Os dados dos contadores de desempenho do sistema estão disponíveis em classes WMI.                                                                                                                                                                            |
| [Suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md)                                       | O [provedor de rotas IP](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI e as classes de rede fornecem dados para endereços IPv4. A partir do Windows Vista, o WMI também fornece suporte limitado para recursos de rede IPv6.                                       |
| [Formato de data e hora](date-and-time-format.md)                                                       | O WMI usa os formatos de data e hora definidos pela especificação CIM da força de tarefas de gerenciamento distribuído. Para obter mais informações, consulte [DMTF](https://www.dmtf.org/).                                                          |
| [Script de acesso ao WMI](scripting-access-to-wmi.md)                                                 | Grave scripts WMI para executar tarefas de gerenciamento.                                                                                                                                                                                                    |
| [Solução de problemas do WMI](wmi-troubleshooting.md)                                                         | Ao acessar dados locais ou remotos do WMI em um aplicativo ou script, você pode receber erros que variam de classes ausentes a acesso negado. Os provedores também têm opções de depuração e de solução de problemas disponíveis.                           |
| [Mais informações](further-information.md)                                                         | Sites, livros e artigos sobre o WMI.                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> <dt>

[Referência de WMI](wmi-reference.md)
</dt> </dl>

 

 
