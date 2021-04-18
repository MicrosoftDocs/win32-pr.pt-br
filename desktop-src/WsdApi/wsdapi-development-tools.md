---
description: As ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (WSD CodeGen, host de depuração WSD e cliente de depuração WSD) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Ferramentas de desenvolvimento do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793296"
---
# <a name="wsdapi-development-tools"></a>Ferramentas de desenvolvimento do WSDAPI

As ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (WSD CodeGen, host de depuração WSD e cliente de depuração WSD) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI. O código-fonte para essas ferramentas não está disponível. As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) converte um contrato WSDL no código C++ gerado, que os desenvolvedores podem chamar diretamente no. Ele lida com a serialização de dados e a representação de transmissão para que os desenvolvedores possam se concentrar na criação de aplicativos. Para obter mais informações sobre WSD CodeGen, consulte [Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md). Essa ferramenta está disponível no Microsoft Windows Software Development Kit (SDK) e no Windows Driver Kit (WDK).

As ferramentas de host de depuração WSD (wsddebug \_host.exe) e de cliente de depuração WSD (wsddebug \_client.exe) ajudam os desenvolvedores a depurar seus clientes e hosts. Essas ferramentas podem ser usadas para verificar e inspecionar o tráfego de WS-Discovery e de troca de metadados. Para obter mais informações sobre o host de depuração WSD e o cliente de depuração WSD, consulte [ferramentas de depuração](debugging-tools.md). Essas ferramentas estão disponíveis apenas no SDK do Windows.

Há uma ferramenta de desenvolvimento adicional chamada [WSDBIT (ferramenta de interoperabilidade básica do WSDAPI)](https://msdn.microsoft.com/library/cc264250.aspx), que está disponível apenas no WDK. Essa ferramenta é usada para testar métodos de serviço, MTOM (mecanismo de otimização de transmissão de mensagens), anexos ou WS-Eventing.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de aplicativos WSD no Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Ferramentas de depuração](debugging-tools.md)
</dt> </dl>

 

 



