---
description: Há dois exemplos de WSDAPI incluídos no SDK do Windows para o Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Exemplos de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661746"
---
# <a name="wsdapi-samples"></a>Exemplos de WSDAPI

Há dois exemplos de WSDAPI incluídos no SDK do Windows para o Windows Server 2008. O código-fonte para os exemplos pode ser encontrado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI. Esta versão do SDK está disponível no centro de [Download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf). Os exemplos não estão disponíveis no SDK do Windows Vista.

O exemplo de cotação de ações (localizado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) demonstra um serviço com a funcionalidade de mensagens básica. O exemplo de serviço de arquivo (localizado em <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ fileservice) demonstra um serviço com funcionalidade avançada, como mensagens assíncronas, anexos e eventos.

Ambos os exemplos incluem os seguintes tipos de arquivos.

-   Arquivos WSDL que contêm as descrições de serviço.
-   [Arquivos de configuração WsdCodeGen](wsdcodegen-configuration-file.md) usados para gerar código WSDAPI.
-   Cabeçalhos e arquivos de origem gerados do C++.
-   Arquivos de implementação de cliente e serviço.
-   Arquivos de solução e projeto do Visual Studio.

Ambos os exemplos implementam hosts de dispositivo ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), proxies de dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) e proxies de serviço ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). Além disso, o exemplo de serviço de arquivo demonstra o uso de mensagens assíncronas ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), anexos ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) e eventos.

Os arquivos FileServiceContract. vcproj e StockQuoteContract. vcproj incluídos com os exemplos chamam [WsdCodeGen](web-services-for-devices-code-generator.md) para gerar arquivos de cabeçalho e origem do C++ a partir do arquivo WSDL especificado no arquivo de configuração WsdCodeGen. Isso significa que, se o arquivo de configuração WSDL ou WsdCodeGen de exemplo for alterado e o projeto de exemplo for recriado, o WsdCodeGen gerará automaticamente novos arquivos de cabeçalho e origem que refletem as alterações. Esse é o método preferencial para a criação de aplicativos WSDAPI. WsdCodeGen geralmente é chamado na linha de comando. Abra o \* arquivo. vcproj relevante para exibir as chamadas de linha de comando do WsdCodeGen de exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de aplicativos WSD no Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



