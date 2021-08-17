---
title: Protocolo WS-Management
description: Um padrão público para trocar remotamente dados de gerenciamento com qualquer dispositivo de computador que implemente o protocolo.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a20900e77d7d686868e00f7067b23fff644255997a14c9d4c1cbdcf3d1951d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742727"
---
# <a name="ws-management-protocol"></a>Protocolo WS-Management

O protocolo WS-Management foi desenvolvido por um grupo de fabricantes de  hardware e software como um padrão público para trocar remotamente dados de gerenciamento com qualquer dispositivo de computador que implementa o protocolo.

## <a name="standards"></a>Padrões

Para obter mais informações sobre WS-Management protocolo, consulte Especificação de [WS-Management (Serviços Web](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)para Gerenciamento).

A intenção do protocolo é fornecer consistência e interoperabilidade para operações de gerenciamento em vários tipos de dispositivos (incluindo firmware) e sistemas operacionais. WS-Management protocolo pode ser estendido à medida que novas operações são identificadas pelo setor de IT.

A implementação atual do protocolo WS-Management baseia-se nas seguintes especificações padrão: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration e WS-Eventing. Para obter mais informações sobre os WS-Management padrão e esquemas XML, consulte <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Mensagens

O WS-Management protocolo fornece um padrão para construir mensagens [*XML*](windows-remote-management-glossary.md) usando vários padrões de serviço Web, como [*WS-Addressing*](windows-remote-management-glossary.md) e [*WS-Transfer.*](windows-remote-management-glossary.md) Esses padrões definem esquemas XML para mensagens de serviço Web. As mensagens se referem a um [*recurso usando*](windows-remote-management-glossary.md) um [*URI de recurso.*](windows-remote-management-glossary.md) O WS-Management protocolo adiciona um conjunto de definições para operações e valores de gerenciamento. Por exemplo, WS-Transfer define as operações Get, Put, Create e Delete para um recurso. WS-Management protocolo adiciona Renomear, Obter Parcial e Put Parcial.

As mensagens seguem as convenções do [*PROTOCOLO SOAP,*](windows-remote-management-glossary.md) que é usado por todos os protocolos de serviço Web.

O exemplo de código a seguir mostra uma mensagem com uma operação Get. Este exemplo é mostrado como um auxílio para entender a aparência das mensagens subjacentes. Você não precisa saber como produzir mensagens SOAP. As mensagens são montadas por Windows Gerenciamento Remoto quando você executa um comando usando a ferramenta de linha de comando **Winrm** ou executa um script escrito com a API de [Script WinRM](winrm-scripting-api.md).

A mensagem é uma solicitação para obter a instância do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com uma propriedade **DeviceID** de "c:" de um servidor chamado RemoteComputer. A solicitação usa o transporte HTTP pela porta 80. A conta que envia a solicitação deve estar no grupo de administradores locais no computador remoto.

Os caracteres antes dos dois-pontos no início de cada marca indicam qual padrão define o elemento XML. Por exemplo, indica que o elemento To é definido pelo padrão WS-Addressing e indica o início do conteúdo do título ` <wsa:To>` `<s:Header>` em uma mensagem SOAP. Esteja ciente de que a maioria da mensagem é composta por elementos XML definidos por SOAP ou WS-Addressing. WS-Management protocolo adiciona MaxEnvelopeSize, Selector e SelectorSet.


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

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Gerenciamento de hardware remoto](remote-hardware-management.md)
</dt> </dl>

 

 