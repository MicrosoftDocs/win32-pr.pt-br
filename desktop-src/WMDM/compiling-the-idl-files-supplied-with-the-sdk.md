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
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800185"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="73ca6-109">Compilando os arquivos IDL fornecidos com o SDK</span><span class="sxs-lookup"><span data-stu-id="73ca6-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="73ca6-110">O SDK do Windows Media Gerenciador de Dispositivos inclui os arquivos de cabeçalho e os arquivos IDL de origem para a maioria desses arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="73ca6-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="73ca6-111">Os arquivos de cabeçalho estão localizados na \\ \\ pasta Inc no caminho de instalação do SDK.</span><span class="sxs-lookup"><span data-stu-id="73ca6-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="73ca6-112">Os arquivos IDL estão localizados na \\ pasta IDL \\ .</span><span class="sxs-lookup"><span data-stu-id="73ca6-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="73ca6-113">Os cabeçalhos pré-compilados são muito mais simples de usar e vários arquivos IDL são combinados em um único cabeçalho fornecido.</span><span class="sxs-lookup"><span data-stu-id="73ca6-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="73ca6-114">No entanto, se você decidir processar seus próprios arquivos de cabeçalho dos arquivos IDL fornecidos, este tópico descreverá quais arquivos IDL criam quais arquivos de cabeçalho e também descreve as dependências de cada arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="73ca6-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="73ca6-115">**IDL equivalente e arquivos de cabeçalho fornecidos**</span><span class="sxs-lookup"><span data-stu-id="73ca6-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="73ca6-116">**INSERI**</span><span class="sxs-lookup"><span data-stu-id="73ca6-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="73ca6-117">**Cabeçalho fornecido equivalente**</span><span class="sxs-lookup"><span data-stu-id="73ca6-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="73ca6-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="73ca6-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ca6-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-119">WMDM.idl</span></span><br/> <span data-ttu-id="73ca6-120">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-120">WMSP.idl</span></span><br/> <span data-ttu-id="73ca6-121">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-121">WMSCP.idl</span></span><br/> <span data-ttu-id="73ca6-122">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="73ca6-123">Mswmdm. h</span><span class="sxs-lookup"><span data-stu-id="73ca6-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="73ca6-124">Todos os quatro arquivos IDL estão incluídos neste cabeçalho único fornecido.</span><span class="sxs-lookup"><span data-stu-id="73ca6-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="73ca6-125">**WMDM. idl** define todas as interfaces de aplicativo e estruturas, constantes e códigos de erro necessários.</span><span class="sxs-lookup"><span data-stu-id="73ca6-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="73ca6-126">**WMSP. idl** define todas as interfaces do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="73ca6-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="73ca6-127">**WMSCP. idl** define todas as interfaces, os valores de GUID e as constantes exigidas por provedores de conteúdo seguro.</span><span class="sxs-lookup"><span data-stu-id="73ca6-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="73ca6-128">**icomponentauthenticate. idl** define a interface [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="73ca6-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="73ca6-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="73ca6-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="73ca6-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="73ca6-131">wmdmlog \_ i. c</span><span class="sxs-lookup"><span data-stu-id="73ca6-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="73ca6-132">Define as interfaces de log.</span><span class="sxs-lookup"><span data-stu-id="73ca6-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="73ca6-133">Ambos os arquivos de cabeçalho fornecidos devem ser usados, em vez de apenas o arquivo. h, devido a um problema com o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="73ca6-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="73ca6-134">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="73ca6-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="73ca6-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="73ca6-136">Define as interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usadas por aplicativos que atualizam DRM em dispositivos ou contagens de planos de execução em dispositivos.</span><span class="sxs-lookup"><span data-stu-id="73ca6-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="73ca6-137">**Dependências de IDL**</span><span class="sxs-lookup"><span data-stu-id="73ca6-137">**IDL Dependencies**</span></span>

<span data-ttu-id="73ca6-138">Vários dos arquivos IDL fornecidos têm dependências de compilação.</span><span class="sxs-lookup"><span data-stu-id="73ca6-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="73ca6-139">Se você planeja compilar os arquivos IDL por conta própria, deve processar essas dependências externas na ordem mostrada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="73ca6-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="73ca6-140">**INSERI**</span><span class="sxs-lookup"><span data-stu-id="73ca6-140">**IDL**</span></span>                    | <span data-ttu-id="73ca6-141">**Dependências**</span><span class="sxs-lookup"><span data-stu-id="73ca6-141">**Dependencies**</span></span>                                                                 |
| <span data-ttu-id="73ca6-142">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="73ca6-143">importe "oaidl. idl";</span><span class="sxs-lookup"><span data-stu-id="73ca6-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="73ca6-144">\#incluir "icomponentauthenticate. idl"</span><span class="sxs-lookup"><span data-stu-id="73ca6-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="73ca6-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-145">WMDM.idl</span></span>                   | <span data-ttu-id="73ca6-146">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="73ca6-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="73ca6-147">WmdmLog. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-147">WmdmLog.idl</span></span>                | <span data-ttu-id="73ca6-148">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="73ca6-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="73ca6-149">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="73ca6-150">Nenhuma dependência externa</span><span class="sxs-lookup"><span data-stu-id="73ca6-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="73ca6-151">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-151">WMSCP.idl</span></span>                  | <span data-ttu-id="73ca6-152">\#incluir "WMDRMDeviceApp. idl"</span><span class="sxs-lookup"><span data-stu-id="73ca6-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="73ca6-153">\#incluir "WMSP. idl"</span><span class="sxs-lookup"><span data-stu-id="73ca6-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="73ca6-154">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="73ca6-154">WMSP.idl</span></span>                   | <span data-ttu-id="73ca6-155">\#incluir "WMDM. idl"</span><span class="sxs-lookup"><span data-stu-id="73ca6-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="73ca6-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73ca6-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ca6-157">**Tarefas comuns a aplicativos e provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="73ca6-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





