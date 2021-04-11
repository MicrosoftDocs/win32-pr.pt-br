---
title: Interface IWMDRMDeviceApp2
description: A interface IWMDRMDeviceApp2 estende o IWMDRMDeviceApp fornecendo uma nova versão do método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDeviceApp2 Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293391"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="3c3a6-105">Interface IWMDRMDeviceApp2</span><span class="sxs-lookup"><span data-stu-id="3c3a6-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="3c3a6-106">A interface **IWMDRMDeviceApp2** estende o [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornecendo uma nova versão do método [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="3c3a6-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="3c3a6-107">O **QueryDeviceStatus2** permite que o chamador consulte um requisito de DRM específico.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="3c3a6-108">Para obter essa interface, chame **CoCreateInstance** e transmita \_ WMDRMDeviceApp CLSID.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="3c3a6-109">Essa interface é definida no arquivo de cabeçalho criado a partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="3c3a6-110">Esse cabeçalho **\# inclui** "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="3c3a6-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="3c3a6-111">Talvez seja necessário alterar esse nome de arquivo para corresponder ao cabeçalho criado a partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="3c3a6-112">Membros</span><span class="sxs-lookup"><span data-stu-id="3c3a6-112">Members</span></span>

<span data-ttu-id="3c3a6-113">A interface **IWMDRMDeviceApp2** herda de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span><span class="sxs-lookup"><span data-stu-id="3c3a6-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="3c3a6-114">**IWMDRMDeviceApp2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3c3a6-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="3c3a6-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c3a6-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c3a6-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c3a6-116">Methods</span></span>

<span data-ttu-id="3c3a6-117">A interface **IWMDRMDeviceApp2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="3c3a6-118">Método</span><span class="sxs-lookup"><span data-stu-id="3c3a6-118">Method</span></span>                                                            | <span data-ttu-id="3c3a6-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c3a6-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="3c3a6-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="3c3a6-121">Consulta um dispositivo em busca de um status ou recurso DRM específico.</span><span class="sxs-lookup"><span data-stu-id="3c3a6-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3c3a6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c3a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3a6-123">**IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="3c3a6-124">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="3c3a6-125">**Interfaces para aplicativos**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="3c3a6-126">**Uso de conteúdo de medição**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





