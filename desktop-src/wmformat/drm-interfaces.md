---
title: Interfaces de cliente DRM do Microsoft Windows Media
description: Interfaces de cliente DRM do Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- SDK do Windows Media Format, interfaces
- DRM (gerenciamento de direitos digitais), interfaces
- DRM (gerenciamento de direitos digitais), interfaces
- APIs estendidas do cliente DRM, interfaces
- APIs estendidas do cliente, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369077"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="6adbc-108">Interfaces de cliente DRM do Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="6adbc-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="6adbc-109">A tabela a seguir descreve as interfaces compatíveis com as APIs de cliente DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6adbc-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="6adbc-110">Interface</span><span class="sxs-lookup"><span data-stu-id="6adbc-110">Interface</span></span>                                                                    | <span data-ttu-id="6adbc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6adbc-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6adbc-112">**IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="6adbc-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="6adbc-113">Fornece a definição para um retorno de chamada de status que você pode implementar para lidar com operações DRM assíncronas.</span><span class="sxs-lookup"><span data-stu-id="6adbc-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="6adbc-114">**IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="6adbc-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="6adbc-115">Fornece um método para descriptografar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6adbc-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="6adbc-116">**IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="6adbc-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="6adbc-117">Fornece um método para criptografar dados no local.</span><span class="sxs-lookup"><span data-stu-id="6adbc-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="6adbc-118">**IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="6adbc-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="6adbc-119">Criptografa dados de blocos não contíguos.</span><span class="sxs-lookup"><span data-stu-id="6adbc-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="6adbc-120">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="6adbc-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="6adbc-121">Extensão da interface **IMFMediaEventGenerator** que fornece um método para cancelar operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="6adbc-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="6adbc-122">**IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="6adbc-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="6adbc-123">Permite a recuperação de informações de status avançadas sobre o progresso da individualização.</span><span class="sxs-lookup"><span data-stu-id="6adbc-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="6adbc-124">**IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="6adbc-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="6adbc-125">Representa uma ou mais licenças no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="6adbc-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="6adbc-126">**IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="6adbc-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="6adbc-127">Permite a recuperação de informações de status detalhadas sobre uma operação de backup ou restauração de licença.</span><span class="sxs-lookup"><span data-stu-id="6adbc-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="6adbc-128">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="6adbc-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="6adbc-129">Habilita operações de gerenciamento para o armazenamento de licença local.</span><span class="sxs-lookup"><span data-stu-id="6adbc-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="6adbc-130">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="6adbc-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="6adbc-131">Fornece opções de gerenciamento adicionais para o armazenamento de licença local.</span><span class="sxs-lookup"><span data-stu-id="6adbc-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="6adbc-132">**IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="6adbc-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="6adbc-133">Permite que os aplicativos consultem os direitos e o estado da licença de um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="6adbc-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="6adbc-134">**IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="6adbc-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="6adbc-135">Fornece métodos necessários para criar um aplicativo de receptor de Microsoft Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="6adbc-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="6adbc-136">**IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="6adbc-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="6adbc-137">Fornece métodos necessários para criar um aplicativo Microsoft Windows Media DRM para dispositivos de rede transmissor.</span><span class="sxs-lookup"><span data-stu-id="6adbc-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="6adbc-138">**IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="6adbc-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="6adbc-139">Fornece métodos que habilitam a aquisição de licenças com a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="6adbc-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="6adbc-140">**IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="6adbc-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="6adbc-141">Cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client.</span><span class="sxs-lookup"><span data-stu-id="6adbc-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="6adbc-142">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="6adbc-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="6adbc-143">Gerencia vários processos relacionados à segurança para o computador cliente e o subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="6adbc-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="6adbc-144">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="6adbc-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="6adbc-145">Gerencia a revogação e a renovação de componentes.</span><span class="sxs-lookup"><span data-stu-id="6adbc-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="6adbc-146">**IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="6adbc-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="6adbc-147">Habilita criptografia e descriptografia de buffers.</span><span class="sxs-lookup"><span data-stu-id="6adbc-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="6adbc-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6adbc-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6adbc-149">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="6adbc-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




