---
description: Um programa de configuração usa a função CreateService para instalar um novo serviço no banco de dados SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Instalação, remoção e enumeração de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647039"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="d26ff-103">Instalação, remoção e enumeração de serviço</span><span class="sxs-lookup"><span data-stu-id="d26ff-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="d26ff-104">Um programa de configuração usa a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para instalar um novo serviço no banco de dados SCM.</span><span class="sxs-lookup"><span data-stu-id="d26ff-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="d26ff-105">Essa função especifica o nome do serviço e fornece informações de configuração que são armazenadas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d26ff-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="d26ff-106">Para obter uma descrição das informações armazenadas no banco de dados para cada serviço, consulte [banco de dados dos serviços instalados](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="d26ff-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="d26ff-107">Para obter um exemplo de código, consulte [instalando um serviço](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="d26ff-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="d26ff-108">Um programa de configuração usa a função [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para remover um serviço instalado do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d26ff-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="d26ff-109">Para obter mais informações, consulte [excluindo um serviço](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="d26ff-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="d26ff-110">Para obter o nome do serviço, chame a função [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) .</span><span class="sxs-lookup"><span data-stu-id="d26ff-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="d26ff-111">O nome de exibição do serviço, usado no miniaplicativo do painel de controle de serviços, pode ser obtido chamando a função [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .</span><span class="sxs-lookup"><span data-stu-id="d26ff-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="d26ff-112">Um programa de configuração de serviço pode usar a função [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar todos os serviços e seus status.</span><span class="sxs-lookup"><span data-stu-id="d26ff-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="d26ff-113">Ele também pode usar a função [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar quais serviços dependem de um objeto de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d26ff-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 



