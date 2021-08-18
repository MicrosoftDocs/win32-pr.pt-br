---
description: as ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (wsd CodeGen, Host de depuração wsd e cliente de depuração wsd) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Ferramentas de desenvolvimento do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdad2d87ffafc337c98743f67ae022eb4d1d11616ac42940157a5785066645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130578"
---
# <a name="wsdapi-development-tools"></a>Ferramentas de desenvolvimento do WSDAPI

as ferramentas de desenvolvimento do WSDAPI incluídas no SDK do Windows (wsd CodeGen, Host de depuração wsd e cliente de depuração wsd) permitem que os desenvolvedores criem e depurem clientes e dispositivos baseados em WSDAPI. O código-fonte para essas ferramentas não está disponível. As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) converte um contrato WSDL no código C++ gerado, que os desenvolvedores podem chamar diretamente no. Ele lida com a serialização de dados e a representação de transmissão para que os desenvolvedores possam se concentrar na criação de aplicativos. Para obter mais informações sobre WSD CodeGen, consulte [Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md). essa ferramenta está disponível no Microsoft Windows Software Development kit (SDK) e no Windows Driver kit (WDK).

As ferramentas de host de depuração WSD (wsddebug \_host.exe) e de cliente de depuração WSD (wsddebug \_client.exe) ajudam os desenvolvedores a depurar seus clientes e hosts. Essas ferramentas podem ser usadas para verificar e inspecionar o tráfego de WS-Discovery e de troca de metadados. Para obter mais informações sobre o host de depuração WSD e o cliente de depuração WSD, consulte [ferramentas de depuração](debugging-tools.md). essas ferramentas estão disponíveis apenas no SDK do Windows.

Há uma ferramenta de desenvolvimento adicional chamada [WSDBIT (ferramenta de interoperabilidade básica do WSDAPI)](https://msdn.microsoft.com/library/cc264250.aspx), que está disponível apenas no WDK. Essa ferramenta é usada para testar métodos de serviço, MTOM (mecanismo de otimização de transmissão de mensagens), anexos ou WS-Eventing.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de aplicativo WSD no Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Serviços Web no gerador de código de dispositivos](web-services-for-devices-code-generator.md)
</dt> <dt>

[Ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Ferramentas de depuração](debugging-tools.md)
</dt> </dl>

 

 



