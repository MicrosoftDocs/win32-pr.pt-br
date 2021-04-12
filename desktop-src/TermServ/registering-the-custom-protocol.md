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
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="c3f4c-103">Registrando o Gerenciador de protocolo</span><span class="sxs-lookup"><span data-stu-id="c3f4c-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="c3f4c-104">Você deve criar pelo menos uma entrada de valor de registro para o Gerenciador de protocolo para que o serviço de Serviços de Área de Trabalho Remota possa instanciá-lo.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="c3f4c-105">Localização do Registro</span><span class="sxs-lookup"><span data-stu-id="c3f4c-105">Registry Location</span></span>

<span data-ttu-id="c3f4c-106">Crie uma chave do registro no seguinte local para cada ouvinte ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que seu protocolo usa.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="c3f4c-107">Neste exemplo, as novas chaves de ouvinte são chamadas *MyListener1* e *MyListener2*.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

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

<span data-ttu-id="c3f4c-108">Para referência, você pode exibir as entradas de valor na chave de ouvinte **RDP-TCP** padrão neste local.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="c3f4c-109">Entradas de valor do registro</span><span class="sxs-lookup"><span data-stu-id="c3f4c-109">Registry Value Entries</span></span>

<span data-ttu-id="c3f4c-110">A chave do ouvinte para o protocolo deve ter uma entrada de valor chamada **\_ objeto LoadableProtocol**</span><span class="sxs-lookup"><span data-stu-id="c3f4c-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="c3f4c-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c3f4c-111">Data type</span></span>
</dt> <dd><span data-ttu-id="c3f4c-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="c3f4c-112">REG_SZ</span></span></dd> <span data-ttu-id="c3f4c-113">Interface </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) O serviço de Serviços de Área de Trabalho Remota usa esse CLSID para instanciar o Gerenciador de protocolo para esse ouvinte depois de encontrar o ouvinte no registro.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="c3f4c-114">Se o provedor de protocolo usar mais de um ouvinte, o serviço de Serviços de Área de Trabalho Remota criará apenas uma instância do Gerenciador de protocolos e o usará para chamar [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) uma vez para cada ouvinte.</span><span class="sxs-lookup"><span data-stu-id="c3f4c-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3f4c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3f4c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3f4c-116">Criando um provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="c3f4c-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="c3f4c-117">Sequência de chamada de método</span><span class="sxs-lookup"><span data-stu-id="c3f4c-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




