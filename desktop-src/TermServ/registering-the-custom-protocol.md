---
title: Registrando o Gerenciador de Protocolos
description: Você deve criar pelo menos uma entrada de valor de registro para o gerenciador de protocolos para que o Serviços de Área de Trabalho Remota possa instaurá-la.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988786"
---
# <a name="registering-the-protocol-manager"></a>Registrando o Gerenciador de Protocolos

Você deve criar pelo menos uma entrada de valor de registro para o gerenciador de protocolos para que o Serviços de Área de Trabalho Remota possa instaurá-la.

## <a name="registry-location"></a>Localização do Registro

Crie uma chave do Registro no seguinte local para cada ouvinte ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que seu protocolo usa. Neste exemplo, as novas chaves de ouvinte são *chamadas MyListener1* e *MyListener2*.

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

Para referência, você pode exibir as entradas de valor na chave **de ouvinte RDP-Tcp** padrão nesse local.

## <a name="registry-value-entries"></a>Entradas de valor do Registro

A chave de ouvinte para o protocolo deve ter uma entrada de valor chamada **Objeto LoadableProtocol \_**<dl> <dt>

Tipo de dados
</dt> <dd>REG_SZ</dd> Interface </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager.)**</a> O Serviços de Área de Trabalho Remota usa essa CLSID para insinuar o gerenciador de protocolo para esse ouvinte depois de encontrar o ouvinte no Registro.

Se o provedor de protocolo usar mais de um ouvinte, o serviço Serviços de Área de Trabalho Remota criará apenas uma instância do gerenciador de protocolo e a usará para chamar [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) uma vez para cada ouvinte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor protocolo RDP dados](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Sequência de chamada de método](method-call-sequence.md)
</dt> </dl>

 

 




