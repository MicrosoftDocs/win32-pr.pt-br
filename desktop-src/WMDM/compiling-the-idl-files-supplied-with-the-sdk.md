---
title: Compilando os arquivos IDL fornecidos com o SDK
description: Compilando os arquivos IDL fornecidos com o SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gerenciador de Dispositivos, arquivos IDL
- Gerenciador de Dispositivos, arquivos IDL
- aplicativos de área de trabalho, arquivos IDL
- provedores de serviço, arquivos IDL
- Guia de programação, arquivos IDL
- arquivos IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444007"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="82c49-109">Compilando os arquivos IDL fornecidos com o SDK</span><span class="sxs-lookup"><span data-stu-id="82c49-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="82c49-110">O SDK do Windows Media Gerenciador de Dispositivos inclui os arquivos de cabeçalho e os arquivos IDL de origem para a maioria desses arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="82c49-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="82c49-111">Os arquivos de cabeçalho estão localizados na \\ \\ pasta Inc no caminho de instalação do SDK.</span><span class="sxs-lookup"><span data-stu-id="82c49-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="82c49-112">Os arquivos IDL estão localizados na \\ pasta IDL \\ .</span><span class="sxs-lookup"><span data-stu-id="82c49-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="82c49-113">Os cabeçalhos pré-compilados são muito mais simples de usar e vários arquivos IDL são combinados em um único cabeçalho fornecido.</span><span class="sxs-lookup"><span data-stu-id="82c49-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="82c49-114">No entanto, se você decidir processar seus próprios arquivos de cabeçalho dos arquivos IDL fornecidos, este tópico descreverá quais arquivos IDL criam quais arquivos de cabeçalho e também descreve as dependências de cada arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="82c49-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="82c49-115">**IDL equivalente e arquivos de cabeçalho fornecidos**</span><span class="sxs-lookup"><span data-stu-id="82c49-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="82c49-116">**INSERI**</span><span class="sxs-lookup"><span data-stu-id="82c49-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="82c49-117">**Cabeçalho fornecido equivalente**</span><span class="sxs-lookup"><span data-stu-id="82c49-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="82c49-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="82c49-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c49-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-119">WMDM.idl</span></span><br/> <span data-ttu-id="82c49-120">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-120">WMSP.idl</span></span><br/> <span data-ttu-id="82c49-121">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-121">WMSCP.idl</span></span><br/> <span data-ttu-id="82c49-122">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="82c49-123">Mswmdm. h</span><span class="sxs-lookup"><span data-stu-id="82c49-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="82c49-124">Todos os quatro arquivos IDL estão incluídos neste cabeçalho único fornecido.</span><span class="sxs-lookup"><span data-stu-id="82c49-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="82c49-125">**WMDM. idl** define todas as interfaces de aplicativo e estruturas, constantes e códigos de erro necessários.</span><span class="sxs-lookup"><span data-stu-id="82c49-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="82c49-126">**WMSP. idl** define todas as interfaces do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="82c49-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="82c49-127">**WMSCP. idl** define todas as interfaces, os valores de GUID e as constantes exigidas por provedores de conteúdo seguro.</span><span class="sxs-lookup"><span data-stu-id="82c49-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="82c49-128">**icomponentauthenticate. idl** define a interface [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="82c49-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="82c49-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="82c49-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="82c49-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="82c49-131">wmdmlog \_ i. c</span><span class="sxs-lookup"><span data-stu-id="82c49-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="82c49-132">Define as interfaces de log.</span><span class="sxs-lookup"><span data-stu-id="82c49-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="82c49-133">Ambos os arquivos de cabeçalho fornecidos devem ser usados, em vez de apenas o arquivo. h, devido a um problema com o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="82c49-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="82c49-134">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="82c49-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="82c49-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="82c49-136">Define as interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usadas por aplicativos que atualizam DRM em dispositivos ou contagens de planos de execução em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="82c49-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="82c49-137">**Dependências de IDL**</span><span class="sxs-lookup"><span data-stu-id="82c49-137">**IDL Dependencies**</span></span>

<span data-ttu-id="82c49-138">Vários dos arquivos IDL fornecidos têm dependências de compilação.</span><span class="sxs-lookup"><span data-stu-id="82c49-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="82c49-139">Se você planeja compilar os arquivos IDL por conta própria, deve processar essas dependências externas na ordem mostrada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="82c49-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="82c49-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="82c49-140">IDL</span></span>                      |   <span data-ttu-id="82c49-141">Dependências</span><span class="sxs-lookup"><span data-stu-id="82c49-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="82c49-142">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="82c49-143">importe "oaidl. idl";</span><span class="sxs-lookup"><span data-stu-id="82c49-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="82c49-144">\#incluir "icomponentauthenticate. idl"</span><span class="sxs-lookup"><span data-stu-id="82c49-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="82c49-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-145">WMDM.idl</span></span>                   | <span data-ttu-id="82c49-146">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="82c49-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="82c49-147">WmdmLog. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-147">WmdmLog.idl</span></span>                | <span data-ttu-id="82c49-148">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="82c49-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="82c49-149">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="82c49-150">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="82c49-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="82c49-151">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-151">WMSCP.idl</span></span>                  | <span data-ttu-id="82c49-152">\#incluir "WMDRMDeviceApp. idl"</span><span class="sxs-lookup"><span data-stu-id="82c49-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="82c49-153">\#incluir "WMSP. idl"</span><span class="sxs-lookup"><span data-stu-id="82c49-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="82c49-154">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="82c49-154">WMSP.idl</span></span>                   | <span data-ttu-id="82c49-155">\#incluir "WMDM. idl"</span><span class="sxs-lookup"><span data-stu-id="82c49-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="82c49-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82c49-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c49-157">**Tarefas comuns a aplicativos e provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="82c49-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





