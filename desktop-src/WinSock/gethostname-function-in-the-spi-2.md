---
description: A consulta WSALookupServiceBegin usa o \_ nome de host SVCID como o GUID de classe de serviço.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Função GetHostName no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814500"
---
# <a name="gethostname-function-in-the-spi"></a>Função GetHostName no SPI

A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa o \_ nome de host SVCID como o GUID de classe de serviço. Se *lpszServiceInstanceName* for nulo ou fizer referência a uma cadeia de caracteres nula (ou seja. ""), o host local deve ser resolvido. Caso contrário, deverá ocorrer uma pesquisa em um nome de host especificado. Para fins de emulação de [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , o \_32.dll Ws2 especificará um ponteiro nulo para *lpszServiceInstanceName* e especificará o \_ nome de retorno de Lup \_ para que o nome do host seja retornado no parâmetro *lpszServiceInstanceName* . Se um aplicativo usar essa consulta e especificar \_ \_ o endereço de retorno de Lup, o host será fornecido em uma estrutura de **\_ informações de CSADDR** . A \_ ação de blob de retorno Lup \_ é indefinida para esta consulta. As informações de porta serão padronizadas como zero, a menos que o *lpszQueryString* faça referência a um serviço como FTP. nesse caso, o endereço de transporte completo do serviço indicado será fornecido.

 

 



