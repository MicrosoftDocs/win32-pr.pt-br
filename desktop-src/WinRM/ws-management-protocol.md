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
# <a name="ws-management-protocol"></a>Protocolo WS-Management

O protocolo WS-Management foi desenvolvido por um grupo de fabricantes de  hardware e software como um padrão público para trocar remotamente dados de gerenciamento com qualquer dispositivo de computador que implementa o protocolo.

## <a name="standards"></a>Padrões

Para obter mais informações sobre o protocolo WS-Management, consulte [especificação de Web Services para gerenciamento (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

A intenção do protocolo é fornecer consistência e interoperabilidade para operações de gerenciamento em vários tipos de dispositivos (incluindo firmware) e sistemas operacionais. O protocolo WS-Management pode ser estendido conforme novas operações são identificadas pelo setor de ti.

A implementação atual do protocolo WS-Management é baseada nas especificações padrão a seguir: HTTPS, SOAP sobre HTTP (WS-I Profile), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Para obter mais informações sobre os padrões de WS-Management e esquemas XML, consulte <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Mensagens

O protocolo WS-Management fornece um padrão para construir [*mensagens*](windows-remote-management-glossary.md) XML usando vários padrões de serviço da Web, como [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer*](windows-remote-management-glossary.md). Esses padrões definem esquemas XML para mensagens de serviço Web. As mensagens se referem a um [*recurso*](windows-remote-management-glossary.md) usando um [*URI de recurso*](windows-remote-management-glossary.md). O protocolo WS-Management adiciona um conjunto de definições para operações e valores de gerenciamento. Por exemplo, WS-Transfer define as operações Get, put, criar e excluir para um recurso. WS-Management protocolo adiciona renomeação, obtenção parcial e Put parcial.

As mensagens seguem as convenções do [*SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) , que é usado por todos os protocolos de serviço Web.

O exemplo de código a seguir mostra uma mensagem com uma operação get. Este exemplo é mostrado como uma ajuda para entender de que forma as mensagens subjacentes se parecem. Você não precisa saber como produzir mensagens SOAP. As mensagens são montadas por Gerenciamento Remoto do Windows quando você executa um comando usando a ferramenta de linha de comando **WinRM** ou executa um script escrito com a [API de script do WinRM](winrm-scripting-api.md).

A mensagem é uma solicitação para obter a instância do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com uma propriedade **DeviceID** de "c:" de um servidor chamado computador_remoto. A solicitação usa o transporte HTTP pela porta 80. A conta que está enviando a solicitação deve estar no grupo local de administradores no computador remoto.

Os caracteres antes dos dois-pontos no início de cada marca indicam qual padrão define o elemento XML. Por exemplo, ` <wsa:To>` indica que o elemento to é definido pelo WS-Addressing padrão e `<s:Header>` indica o início do conteúdo do cabeçalho em uma mensagem SOAP. Lembre-se de que a maior parte da mensagem é composta de elementos XML definidos por SOAP ou WS-Addressing. WS-Management protocolo adiciona MaxEnvelopeSize, selector e SelectorSet.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Gerenciamento de hardware remoto](remote-hardware-management.md)
</dt> </dl>

 

 