---
title: Arquivos de código para o exemplo de provedor de origem
description: Arquivos de código para o exemplo de provedor de origem
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de provedor de serviço
- Gerenciador de Dispositivos, exemplo de provedor de serviço
- provedores de serviços, exemplos
- exemplos, provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084085"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="7cc2b-109">Arquivos de código para o exemplo de provedor de origem</span><span class="sxs-lookup"><span data-stu-id="7cc2b-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="7cc2b-110">O projeto de provedor de origem de exemplo inclui os seguintes arquivos de código-fonte, com cabeçalhos associados:</span><span class="sxs-lookup"><span data-stu-id="7cc2b-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="7cc2b-111">Arquivo</span><span class="sxs-lookup"><span data-stu-id="7cc2b-111">File</span></span>                   | <span data-ttu-id="7cc2b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cc2b-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc2b-113">hdsppch. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-113">hdsppch.cpp</span></span>            | <span data-ttu-id="7cc2b-114">Inclui arquivos ATL padrão.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="7cc2b-115">chave. c</span><span class="sxs-lookup"><span data-stu-id="7cc2b-115">key.c</span></span>                  | <span data-ttu-id="7cc2b-116">Contém uma chave de autenticação fictícia.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="7cc2b-117">loghelp. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-117">loghelp.cpp</span></span>            | <span data-ttu-id="7cc2b-118">Contém funções que registram a atividade e os erros usando a classe **WMDMLogger** , que é implementada no arquivo do sistema WMDMLOG.dll.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="7cc2b-119">MDServiceProvider. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="7cc2b-120">Implementa uma classe, CMDServiceProvider, que implementa as interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="7cc2b-121">MDSP. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-121">mdsp.cpp</span></span>               | <span data-ttu-id="7cc2b-122">Ponto de entrada de DLL e código de registro.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="7cc2b-123">MDSPDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="7cc2b-124">Implementa uma classe, CMDSPDevice, que implementa as interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="7cc2b-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="7cc2b-125">MDSPEnumDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="7cc2b-126">Implementa uma classe, CMDSPEnumDevice, que implementa a interface [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .</span><span class="sxs-lookup"><span data-stu-id="7cc2b-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="7cc2b-127">MDSPEnumStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="7cc2b-128">Implementa uma classe, CMDSPEnumStorage, que implementa a interface [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="7cc2b-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="7cc2b-129">MDSPStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="7cc2b-130">Implementa uma classe, CMDSPStorage, que implementa as interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .</span><span class="sxs-lookup"><span data-stu-id="7cc2b-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="7cc2b-131">MDSPStorageGlobals. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="7cc2b-132">Implementa uma classe, CMDSPStorageGlobals, que implementa a interface [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .</span><span class="sxs-lookup"><span data-stu-id="7cc2b-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="7cc2b-133">MDSPutil. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="7cc2b-134">Contém várias funções de utilitário para gerenciamento de dispositivos e arquivos.</span><span class="sxs-lookup"><span data-stu-id="7cc2b-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="7cc2b-135">PropPage. cpp</span><span class="sxs-lookup"><span data-stu-id="7cc2b-135">proppage.cpp</span></span>           | <span data-ttu-id="7cc2b-136">Implementa uma classe, CPropPage, que herda as classes ATL **IPropertyPageImpl** (para implementar IPropertyPage) e **CDialogImpl**, que herda a classe ATL CDialogImpl (para gerenciar janelas e mensagens).</span><span class="sxs-lookup"><span data-stu-id="7cc2b-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7cc2b-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cc2b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc2b-138">**Provedor de serviços de exemplo**</span><span class="sxs-lookup"><span data-stu-id="7cc2b-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




