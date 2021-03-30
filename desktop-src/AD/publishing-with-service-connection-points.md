---
title: Publicando com pontos de conexão de serviço
description: O esquema de Active Directory define uma classe de objeto serviceConnectionPoint (SCP) para tornar mais fácil para um serviço publicar dados específicos do serviço no diretório.
ms.assetid: 3544aa64-ecb0-48a1-ae49-05247a983842
ms.tgt_platform: multiple
keywords:
- Publicando com pontos de conexão de serviço AD
- AD de pontos de conexão de serviço
- pontos de conexão de serviço AD, publicando com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a458822f6c5e4d764b2e330c7ba084021b586548
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634927"
---
# <a name="publishing-with-service-connection-points"></a>Publicando com pontos de conexão de serviço

O esquema de Active Directory define uma classe de objeto **serviceConnectionPoint** (SCP) para tornar mais fácil para um serviço publicar dados específicos do serviço no diretório. Os clientes do serviço usam os dados em um SCP para localizar, conectar e autenticar uma instância do serviço.

Esta seção fornece uma visão geral dos pontos de conexão de serviço e exemplos de código que mostram como um aplicativo cliente/serviço usa o SCPs.

O exemplo de código segue estas etapas para implementar a publicação de serviço com SCPs.

Para obter mais informações e um exemplo de código que executa essas etapas, consulte [criando um ponto de conexão de serviço](creating-a-service-connection-point.md).

**Para criar SCPs no diretório na instalação do serviço**

1.  Associe-se ao objeto de computador do computador host no qual a instância de serviço está instalada.
2.  Crie um objeto SCP como um filho do objeto Computer, especificando os valores iniciais para os atributos do SCP.
3.  Defina as ACEs (entradas de controle de acesso) no descritor de segurança do objeto SCP para permitir que o serviço modifique as propriedades do SCP em tempo de execução.
4.  Armazene o **objectGUID** do SCP no registro no computador host do serviço.

Para obter mais informações e um exemplo de código que executa essas etapas, consulte [atualizando um ponto de conexão de serviço](updating-a-service-connection-point.md).

**Para atualizar os atributos do SCP na inicialização do serviço**

1.  Recupere o **objectGUID** do registro e use-o para associar ao scp.
2.  Recupere atributos, como **serviceDNSName** e **SERVICEBINDINGINFORMATION**, do SCP. Compare esses valores com os valores atuais e atualize o SCP, se necessário.

Para obter mais informações e um exemplo de código que executa essas etapas, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).

**Para localizar e usar um SCP por um aplicativo cliente**

1.  Associe-se ao catálogo global e pesquise objetos com um atributo de **palavras-chave** que corresponda ao GUID do produto do serviço. Cada objeto encontrado é uma instância do serviço. Selecione uma instância e recupere o nome distinto do SCP.
2.  Use o nome distinto para associar ao SCP.
3.  Recupere os valores de vários atributos do SCP, como **serviceDNSName** e **ServiceBindingInformation**. Use esses valores para se conectar e autenticar a instância do serviço.

Para obter mais informações sobre quais funções podem criar e atualizar um SCP, consulte [problemas de segurança para publicação de serviço](security-issues-for-service-publication.md).

Para obter mais informações sobre onde criar um SCP, consulte [onde criar um ponto de conexão de serviço](where-to-create-a-service-connection-point.md).

Para obter mais informações sobre o tipo de dados a ser armazenado em um SCP, consulte [Propriedades do ponto de conexão de serviço](service-connection-point-properties.md).

Para obter mais informações sobre como um instalador de serviço e o serviço funcionam em conjunto para manter os dados atuais em um SCP, consulte [criando e mantendo um ponto de conexão de serviço](creating-and-maintaining-a-service-connection-point.md).

 

 




