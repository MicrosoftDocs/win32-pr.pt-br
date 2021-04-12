---
title: Parâmetros do dispositivo
description: Parâmetros do dispositivo
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media Gerenciador de Dispositivos, parâmetros do dispositivo
- Gerenciador de Dispositivos, parâmetros do dispositivo
- Guia de programação, parâmetros do dispositivo
- provedores de serviço, parâmetros do dispositivo
- criando provedores de serviços, parâmetros de dispositivo
- parâmetros do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292053"
---
# <a name="device-parameters"></a><span data-ttu-id="f6716-109">Parâmetros do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f6716-109">Device Parameters</span></span>

<span data-ttu-id="f6716-110">O Windows Media Gerenciador de Dispositivos usa parâmetros de dispositivo para controlar o comportamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6716-110">Windows Media Device Manager uses device parameters to control the behavior of a device.</span></span> <span data-ttu-id="f6716-111">Esses parâmetros são adicionados ao registro conforme especificado no arquivo de instalação do dispositivo (arquivo INF).</span><span class="sxs-lookup"><span data-stu-id="f6716-111">These parameters are added to the registry as specified in the device's installation file (INF file).</span></span> <span data-ttu-id="f6716-112">A tabela a seguir lista os parâmetros de dispositivo que o Windows Media Gerenciador de Dispositivos consulta.</span><span class="sxs-lookup"><span data-stu-id="f6716-112">The following table lists the device parameters that Windows Media Device Manager queries.</span></span>



| <span data-ttu-id="f6716-113">Nome do parâmetro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f6716-113">Device parameter name</span></span> | <span data-ttu-id="f6716-114">Tipo de dados do registro</span><span class="sxs-lookup"><span data-stu-id="f6716-114">Registry data type</span></span> | <span data-ttu-id="f6716-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6716-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6716-116">*WMDMSPCLSID*</span><span class="sxs-lookup"><span data-stu-id="f6716-116">*WMDMSPCLSID*</span></span>         | <span data-ttu-id="f6716-117">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="f6716-117">**REG\_SZ**</span></span>        | <span data-ttu-id="f6716-118">Valor que especifica o CLSID do provedor de serviços que controla este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6716-118">Value that specifies the CLSID of the service provider controlling this device.</span></span> <span data-ttu-id="f6716-119">Esse parâmetro é obrigatório para suporte a PnP.</span><span class="sxs-lookup"><span data-stu-id="f6716-119">This parameter is mandatory for PnP support.</span></span><br/> <span data-ttu-id="f6716-120">O valor do parâmetro deve ser o CLSID, não o ProgID do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="f6716-120">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span> <span data-ttu-id="f6716-121">Esse parâmetro é obrigatório para dar suporte a Plug and Play (PnP) no Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f6716-121">This parameter is mandatory to support Plug and Play (PnP) under Windows Media Device Manager.</span></span> <span data-ttu-id="f6716-122">Para obter mais informações, consulte [habilitando PNP para dispositivos](enabling-pnp-for-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f6716-122">For more information, see [Enabling PnP for Devices](enabling-pnp-for-devices.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f6716-123">*OptimalTransferSize*</span><span class="sxs-lookup"><span data-stu-id="f6716-123">*OptimalTransferSize*</span></span> | <span data-ttu-id="f6716-124">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6716-124">**REG\_DWORD**</span></span>     | <span data-ttu-id="f6716-125">Valor opcional que especifica o tamanho de transferência preferencial que o Windows Media Gerenciador de Dispositivos usa durante as operações de leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="f6716-125">Optional value that specifies the preferred transfer size that Windows Media Device Manager uses during read and write operations.</span></span> <span data-ttu-id="f6716-126">Se não for fornecido, será usado um tamanho de transferência padrão.</span><span class="sxs-lookup"><span data-stu-id="f6716-126">If it is not supplied, a default transfer size is used.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f6716-127">*UseMetadataViews*</span><span class="sxs-lookup"><span data-stu-id="f6716-127">*UseMetadataViews*</span></span>    | <span data-ttu-id="f6716-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6716-128">**REG\_DWORD**</span></span>     | <span data-ttu-id="f6716-129">Parâmetro opcional que especifica se o Windows Media Gerenciador de Dispositivos organiza o conteúdo por metadados ao apresentar o conteúdo do dispositivo aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f6716-129">Optional parameter that specifies whether Windows Media Device Manager organizes the content by metadata while presenting device content to applications.</span></span> <span data-ttu-id="f6716-130">Se não for especificado, o valor padrão será 0.</span><span class="sxs-lookup"><span data-stu-id="f6716-130">If not specified, the default value is 0.</span></span><br/> <span data-ttu-id="f6716-131">Quando os aplicativos enumeram o conteúdo nos armazenamentos de um player de áudio portátil, o Windows Media Gerenciador de Dispositivos pode apresentar o conteúdo organizado por metadados.</span><span class="sxs-lookup"><span data-stu-id="f6716-131">When applications enumerate the content on the storages of a portable audio player, Windows Media Device Manager can present the content organized by metadata.</span></span> <span data-ttu-id="f6716-132">Isso é especialmente útil para dispositivos com grande capacidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f6716-132">This is especially useful for devices with large storage capacity.</span></span><br/> <span data-ttu-id="f6716-133">Aplicativos e dispositivos têm a capacidade de controlar esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="f6716-133">Applications and devices have the ability to control this behavior.</span></span> <span data-ttu-id="f6716-134">Os dispositivos indicam sua preferência por meio do parâmetro de dispositivo *UseMetadataViews*.</span><span class="sxs-lookup"><span data-stu-id="f6716-134">Devices indicate their preference through the device parameter *UseMetadataViews*.</span></span><br/> <span data-ttu-id="f6716-135">Há suporte para os dois valores inteiros a seguir:</span><span class="sxs-lookup"><span data-stu-id="f6716-135">The following two integer values are supported:</span></span><br/> <span data-ttu-id="f6716-136">Solicita que o conteúdo seja apresentado aos aplicativos exatamente como organizado no sistema de arquivos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6716-136">Requests that content be presented to the applications exactly as organized on the file system of the device.</span></span><br/> <span data-ttu-id="f6716-137">Solicita que o conteúdo seja apresentado aos aplicativos organizados por metadados.</span><span class="sxs-lookup"><span data-stu-id="f6716-137">Requests that the content be presented to the applications organized by metadata.</span></span><br/> |
| <span data-ttu-id="f6716-138">*ShowInShell*</span><span class="sxs-lookup"><span data-stu-id="f6716-138">*ShowInShell*</span></span>         | <span data-ttu-id="f6716-139">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6716-139">**REG\_DWORD**</span></span>     | <span data-ttu-id="f6716-140">Parâmetro opcional que especifica se o dispositivo deve aparecer no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f6716-140">Optional parameter that specifies whether the device should appear in Windows Explorer.</span></span> <span data-ttu-id="f6716-141">O valor 1 indica que o dispositivo deve aparecer no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="f6716-141">The value 1 indicates that the device should appear in Windows Explorer.</span></span> <span data-ttu-id="f6716-142">Para obter mais informações, consulte [requisitos para players de áudio portáteis a serem exibidos no Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="f6716-142">For more information, see [Requirements for Portable Audio Players to Appear in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f6716-143">*UseExtendedWmdm*</span><span class="sxs-lookup"><span data-stu-id="f6716-143">*UseExtendedWmdm*</span></span>     | <span data-ttu-id="f6716-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f6716-144">**REG\_DWORD**</span></span>     | <span data-ttu-id="f6716-145">Parâmetro opcional que alerta o Windows Media Gerenciador de Dispositivos que o provedor de serviços dá suporte a **IMDSPDevice3**, **IMDSPObject2** e **IMDSPStorage4**.</span><span class="sxs-lookup"><span data-stu-id="f6716-145">Optional parameter that alerts Windows Media Device Manager that the service provider supports **IMDSPDevice3**, **IMDSPObject2**, and **IMDSPStorage4**.</span></span> <span data-ttu-id="f6716-146">Sem esse sinalizador, o Windows Media Gerenciador de Dispositivos nunca chamará essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f6716-146">Without this flag, Windows Media Device Manager will never call these interfaces.</span></span> <span data-ttu-id="f6716-147">O valor 1 indica que há suporte para essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f6716-147">The value 1 indicates that these interfaces are supported.</span></span><br/> <span data-ttu-id="f6716-148">Esse sinalizador é necessário para provedores de serviços que sincronizam com o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f6716-148">This flag is required for service providers that synchronize with Windows Media Player.</span></span> <span data-ttu-id="f6716-149">(Consulte [habilitando a sincronização com o Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span><span class="sxs-lookup"><span data-stu-id="f6716-149">(See [Enabling Synchronization with Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="f6716-150">**Codificando o arquivo INF**</span><span class="sxs-lookup"><span data-stu-id="f6716-150">**Coding the INF file**</span></span>

<span data-ttu-id="f6716-151">O código de exemplo a seguir do arquivo INF de um dispositivo demonstra a definição de alguns parâmetros de dispositivo durante a instalação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6716-151">The following example code from a device's INF file demonstrates setting some device parameters during device installation.</span></span>


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a><span data-ttu-id="f6716-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6716-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6716-153">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="f6716-153">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="f6716-154">**Interface IMDServiceProvider2**</span><span class="sxs-lookup"><span data-stu-id="f6716-154">**IMDServiceProvider2 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[<span data-ttu-id="f6716-155">**IMDServiceProvider2:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="f6716-155">**IMDServiceProvider2::CreateDevice**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[<span data-ttu-id="f6716-156">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="f6716-156">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





