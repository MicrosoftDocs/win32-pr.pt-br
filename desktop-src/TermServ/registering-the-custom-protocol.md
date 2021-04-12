---
title: Registrando o Gerenciador de protocolo
description: Você deve criar pelo menos uma entrada de valor de registro para o Gerenciador de protocolo para que o serviço de Serviços de Área de Trabalho Remota possa instanciá-lo.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363820"
---
# <a name="registering-the-protocol-manager"></a>Registrando o Gerenciador de protocolo

Você deve criar pelo menos uma entrada de valor de registro para o Gerenciador de protocolo para que o serviço de Serviços de Área de Trabalho Remota possa instanciá-lo.

## <a name="registry-location"></a>Localização do Registro

Crie uma chave do registro no seguinte local para cada ouvinte ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que seu protocolo usa. Neste exemplo, as novas chaves de ouvinte são chamadas *MyListener1* e *MyListener2*.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Para referência, você pode exibir as entradas de valor na chave de ouvinte **RDP-TCP** padrão neste local.

## <a name="registry-value-entries"></a>Entradas de valor do registro

A chave do ouvinte para o protocolo deve ter uma entrada de valor chamada **\_ objeto LoadableProtocol**<dl> <dt>

Tipo de dados
</dt> <dd>REG_SZ</dd> Interface </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) O serviço de Serviços de Área de Trabalho Remota usa esse CLSID para instanciar o Gerenciador de protocolo para esse ouvinte depois de encontrar o ouvinte no registro.

Se o provedor de protocolo usar mais de um ouvinte, o serviço de Serviços de Área de Trabalho Remota criará apenas uma instância do Gerenciador de protocolos e o usará para chamar [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) uma vez para cada ouvinte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de protocolo RDP](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Sequência de chamada de método](method-call-sequence.md)
</dt> </dl>

 

 




