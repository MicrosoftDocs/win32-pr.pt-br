---
description: O Microsoft&\# 160; O provedor Win32 recupera e atualiza dados relevantes para sistemas Windows&\# 8212; dados como as configurações atuais de variáveis de ambiente e os atributos de um disco lógico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Provedor Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646250"
---
# <a name="win32-provider"></a><span data-ttu-id="dfe4a-103">Provedor Win32</span><span class="sxs-lookup"><span data-stu-id="dfe4a-103">Win32 Provider</span></span>

<span data-ttu-id="dfe4a-104">O provedor Microsoft Win32 recupera e atualiza os dados relevantes para sistemas Windows — dados como as configurações atuais de variáveis de ambiente e os atributos de um disco lógico.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="dfe4a-105">Com o provedor do Win32, os aplicativos de gerenciamento podem usar o WMI para acessar facilmente esses dados.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="dfe4a-106">O provedor Win32 recupera suas informações fazendo chamadas de função do Windows e consultando o registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="dfe4a-107">O provedor Win32 define as classes usadas para descrever o hardware ou o software disponível em sistemas Windows e as relações entre eles.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="dfe4a-108">Como um provedor de instância e método, o provedor Win32 implementa a interface [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como os seguintes métodos de [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) :</span><span class="sxs-lookup"><span data-stu-id="dfe4a-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="dfe4a-109">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="dfe4a-110">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="dfe4a-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="dfe4a-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="dfe4a-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="dfe4a-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="dfe4a-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="dfe4a-115">A tabela a seguir lista as categorias de classe do provedor do Win32.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="dfe4a-116">Classes</span><span class="sxs-lookup"><span data-stu-id="dfe4a-116">Classes</span></span>                                                                             | <span data-ttu-id="dfe4a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfe4a-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="dfe4a-118">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="dfe4a-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="dfe4a-119">Objetos relacionados ao hardware.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="dfe4a-120">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="dfe4a-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="dfe4a-121">Objetos relacionados ao sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="dfe4a-122">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="dfe4a-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="dfe4a-123">Dados de desempenho brutos e calculados dos contadores de desempenho.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="dfe4a-124">Classes de gerenciamento de serviço WMI</span><span class="sxs-lookup"><span data-stu-id="dfe4a-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="dfe4a-125">Gerenciamento do WMI.</span><span class="sxs-lookup"><span data-stu-id="dfe4a-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="dfe4a-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfe4a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe4a-127">Provedor WMI do CIMWin32</span><span class="sxs-lookup"><span data-stu-id="dfe4a-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
