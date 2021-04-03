---
title: Protocolo WS-Management
description: Um padrão público para a troca remota de dados de gerenciamento com qualquer dispositivo de computador que implementa o protocolo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084876"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="7e2b7-103">Protocolo WS-Management</span><span class="sxs-lookup"><span data-stu-id="7e2b7-103">WS-Management Protocol</span></span>

<span data-ttu-id="7e2b7-104">O protocolo WS-Management foi desenvolvido por um grupo de fabricantes de  hardware e software como um padrão público para trocar remotamente dados de gerenciamento com qualquer dispositivo de computador que implementa o protocolo.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="7e2b7-105">Padrões</span><span class="sxs-lookup"><span data-stu-id="7e2b7-105">Standards</span></span>

<span data-ttu-id="7e2b7-106">Para obter mais informações sobre o protocolo WS-Management, consulte [especificação de Web Services para gerenciamento (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="7e2b7-107">A intenção do protocolo é fornecer consistência e interoperabilidade para operações de gerenciamento em vários tipos de dispositivos (incluindo firmware) e sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="7e2b7-108">O protocolo WS-Management pode ser estendido conforme novas operações são identificadas pelo setor de ti.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="7e2b7-109">A implementação atual do protocolo WS-Management é baseada nas especificações padrão a seguir: HTTPS, SOAP sobre HTTP (WS-I Profile), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="7e2b7-110">Para obter mais informações sobre os padrões de WS-Management e esquemas XML, consulte <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="7e2b7-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="7e2b7-111">Mensagens</span><span class="sxs-lookup"><span data-stu-id="7e2b7-111">Messages</span></span>

<span data-ttu-id="7e2b7-112">O protocolo WS-Management fornece um padrão para construir [*mensagens*](windows-remote-management-glossary.md) XML usando vários padrões de serviço da Web, como [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="7e2b7-113">Esses padrões definem esquemas XML para mensagens de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="7e2b7-114">As mensagens se referem a um [*recurso*](windows-remote-management-glossary.md) usando um [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="7e2b7-115">O protocolo WS-Management adiciona um conjunto de definições para operações e valores de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="7e2b7-116">Por exemplo, WS-Transfer define as operações Get, put, criar e excluir para um recurso.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="7e2b7-117">WS-Management protocolo adiciona renomeação, obtenção parcial e Put parcial.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="7e2b7-118">As mensagens seguem as convenções do [*SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) , que é usado por todos os protocolos de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="7e2b7-119">O exemplo de código a seguir mostra uma mensagem com uma operação get.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="7e2b7-120">Este exemplo é mostrado como uma ajuda para entender de que forma as mensagens subjacentes se parecem.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="7e2b7-121">Você não precisa saber como produzir mensagens SOAP.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="7e2b7-122">As mensagens são montadas por Gerenciamento Remoto do Windows quando você executa um comando usando a ferramenta de linha de comando **WinRM** ou executa um script escrito com a [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7e2b7-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="7e2b7-123">A mensagem é uma solicitação para obter a instância do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com uma propriedade **DeviceID** de "c:" de um servidor chamado computador_remoto.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="7e2b7-124">A solicitação usa o transporte HTTP pela porta 80.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="7e2b7-125">A conta que está enviando a solicitação deve estar no grupo local de administradores no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="7e2b7-126">Os caracteres antes dos dois-pontos no início de cada marca indicam qual padrão define o elemento XML.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="7e2b7-127">Por exemplo, ` <wsa:To>` indica que o elemento to é definido pelo WS-Addressing padrão e `<s:Header>` indica o início do conteúdo do cabeçalho em uma mensagem SOAP.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="7e2b7-128">Lembre-se de que a maior parte da mensagem é composta de elementos XML definidos por SOAP ou WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="7e2b7-129">WS-Management protocolo adiciona MaxEnvelopeSize, selector e SelectorSet.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="7e2b7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e2b7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e2b7-131">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="7e2b7-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="7e2b7-132">Gerenciamento de hardware remoto</span><span class="sxs-lookup"><span data-stu-id="7e2b7-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 