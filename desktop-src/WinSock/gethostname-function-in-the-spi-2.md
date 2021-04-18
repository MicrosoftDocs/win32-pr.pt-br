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
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="76d24-103">Função GetHostName no SPI</span><span class="sxs-lookup"><span data-stu-id="76d24-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="76d24-104">A consulta [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa o \_ nome de host SVCID como o GUID de classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="76d24-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="76d24-105">Se *lpszServiceInstanceName* for nulo ou fizer referência a uma cadeia de caracteres nula (ou seja.</span><span class="sxs-lookup"><span data-stu-id="76d24-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="76d24-106">""), o host local deve ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="76d24-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="76d24-107">Caso contrário, deverá ocorrer uma pesquisa em um nome de host especificado.</span><span class="sxs-lookup"><span data-stu-id="76d24-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="76d24-108">Para fins de emulação de [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) , o \_32.dll Ws2 especificará um ponteiro nulo para *lpszServiceInstanceName* e especificará o \_ nome de retorno de Lup \_ para que o nome do host seja retornado no parâmetro *lpszServiceInstanceName* .</span><span class="sxs-lookup"><span data-stu-id="76d24-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="76d24-109">Se um aplicativo usar essa consulta e especificar \_ \_ o endereço de retorno de Lup, o host será fornecido em uma estrutura de **\_ informações de CSADDR** .</span><span class="sxs-lookup"><span data-stu-id="76d24-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="76d24-110">A \_ ação de blob de retorno Lup \_ é indefinida para esta consulta.</span><span class="sxs-lookup"><span data-stu-id="76d24-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="76d24-111">As informações de porta serão padronizadas como zero, a menos que o *lpszQueryString* faça referência a um serviço como FTP. nesse caso, o endereço de transporte completo do serviço indicado será fornecido.</span><span class="sxs-lookup"><span data-stu-id="76d24-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



