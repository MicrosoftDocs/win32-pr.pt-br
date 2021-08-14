---
title: Como os clientes compõem o SPN de um serviço
description: Para autenticar um serviço, um aplicativo cliente compõe um SPN para a instância de serviço à qual ele deve se conectar.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Como os clientes compõem o AD SPN de um serviço
- nome da entidade de serviço AD, como os clientes compõem o SPN de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06c3531ac329af1a4c4fa7721b5d575ce762d86f15767278ad9a348e7956cfa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188181"
---
# <a name="how-clients-compose-a-services-spn"></a>Como os clientes compõem o SPN de um serviço

Para autenticar um serviço, um aplicativo cliente compõe um SPN para a instância de serviço à qual ele deve se conectar. O aplicativo cliente pode usar a função [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para compor um SPN. O cliente especifica os componentes do SPN usando dados conhecidos ou dados recuperados de fontes diferentes do serviço em si.

A forma de um SPN é como mostrado no seguinte formato:


```C++
<service class>/<host>:<port>/<service name>
```



Neste formulário, " &lt; classe de serviço &gt; " e " &lt; host &gt; " são necessários. " &lt; porta &gt; " e " &lt; nome do serviço &gt; " opcionais.

Normalmente, o cliente reconhece a parte de " &lt; classe &gt; de serviço" do nome e reconhece qual dos componentes opcionais incluir no SPN. O cliente pode recuperar componentes do SPN de fontes como um SCP (ponto de conexão de serviço) ou entrada de usuário. Por exemplo, o cliente pode ler o atributo **serviceDNSName** do SCP de um serviço para obter o &lt; componente "host &gt; ". O atributo **serviceDNSName** contém o nome DNS do servidor no qual a instância de serviço está em execução ou o nome DNS dos registros SRV que contêm os dados do host para réplicas de serviço. O &lt; componente "nome do serviço &gt; ", usado somente para serviços replicáveis, pode ser o nome distinto do SCP do serviço, o nome DNS do domínio servido pelo serviço ou o nome DNS dos registros SRV ou MX.

para obter mais informações e um exemplo de código usado para compor um SPN para um serviço, consulte [como um cliente autentica um serviço de soquetes de Windows baseado em SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).

Para obter mais informações e uma descrição dos componentes do SPN, consulte [formatos de nome para SPNs exclusivos](name-formats-for-unique-spns.md).

 

 




