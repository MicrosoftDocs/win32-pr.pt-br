---
description: Uma plataforma de desenvolvimento para a criação de autoridades de certificação para empresas ou aplicativos de Internet seguros.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Arquitetura de serviços de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b7e0545b2f0fe0dd8c30d1863ffdf52c64a9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164734"
---
# <a name="certificate-services-architecture"></a>Arquitetura de serviços de certificados

Os serviços de certificados são uma plataforma de desenvolvimento para a criação de autoridades de certificação para empresas ou aplicativos de Internet seguros. Uma autoridade de certificação configurada e operacional permitirá que um site emita, acompanhe, gerencie e revogue certificados com sobrecarga de administração mínima e segurança máxima.

Os serviços de certificados consistem no mecanismo do servidor, no banco de dados do servidor e em um conjunto de módulos e ferramentas que funcionam juntos para funcionar como uma autoridade de certificação. Os aplicativos externos, os módulos e as ferramentas de administração usam as interfaces Component Object Model (COM) para interagir com o mecanismo do servidor. O diagrama a seguir mostra as interfaces usadas pelo mecanismo do servidor:

![arquitetura de serviços de certificados](images/certapi.png)

Um sistema de certificação operacional normalmente terá quatro subsistemas principais.



| Subsistema             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente                | O cliente é o software usado pelo usuário final para gerar uma [*solicitação de certificado*](../secgloss/c-gly.md), enviar a solicitação e receber o certificado concluído. Um exemplo de cliente é o Microsoft Internet Explorer versão 5. O cliente normalmente irá interagir com uma interface personalizada mantida pelo aplicativo intermediário.                                                                                                                                                                                                                                                                                              |
| Intermediário          | O intermediário é um subsistema que consiste no aplicativo intermediário e na interface do cliente de serviços de certificados (*cliente Web dos serviços de certificados* no programa de instalação). O aplicativo intermediário interage diretamente com o cliente, recebendo solicitações de certificado e retornando certificados concluídos. Ele se comunica com o mecanismo do servidor por meio da interface de cliente dos serviços de certificados, que contém as interfaces com [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) e [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) . Um exemplo de aplicativo intermediário é o Microsoft Serviços de Informações da Internet. O aplicativo intermediário pode ser implementado inteiramente por meio de Active Server páginas. |
| Servidor                | O servidor é o sistema que cria o certificado. Além do mecanismo do servidor, dois componentes configuráveis são incluídos; o módulo de política e o módulo de saída. O módulo de política interage com o mecanismo de servidor por meio das interfaces [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Módulos de saída (pode haver mais de um) interagir com o mecanismo do servidor por meio das interfaces [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) e [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) .                                                                                                                                                                                       |
| Cliente administrativo | O cliente administrativo é o sistema que monitora e gerencia certificados e solicitações. O cliente administrativo usa a interface [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) para se comunicar com o mecanismo do servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Para obter mais informações sobre a arquitetura de serviços de certificados, consulte [interfaces de criptografia](cryptography-interfaces.md), [criando um certificado](building-a-certificate.md)e os tópicos a seguir.



| Seção                                      | Conteúdo                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Módulos de política](policy-modules.md)         | Programas personalizáveis que podem ser usados durante a avaliação de [*solicitações de certificado*](../secgloss/c-gly.md); esses programas impõem as regras pelas quais os serviços de certificado emite ou negam a solicitação. |
| [Módulos de saída](exit-modules.md)             | Programas personalizáveis que recebem notificações do mecanismo do servidor quando ocorrem operações, como quando um certificado é emitido.                                                                                                                                       |
| [Manipuladores de extensão](extension-handlers.md) | Objetos COM que fornecem rotinas para codificar as extensões e os tipos de dados mais complexos.                                                                                                                                                                                 |
| [intermediários](intermediaries.md)         | Programas que se comunicam com aplicativos cliente para permitir o envio de solicitações de certificado.                                                                                                                                                                        |



 

 

 
