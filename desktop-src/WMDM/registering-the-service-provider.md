---
title: Registrando o provedor de serviços
description: Registrando o provedor de serviços
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Gerenciador de Dispositivos, registrando provedores de serviço
- Gerenciador de Dispositivos, registrando provedores de serviço
- Guia de programação, registrando provedores de serviço
- provedores de serviços, registrando provedores de serviços
- criando provedores de serviços, registrando provedores de serviços
- registrando provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005056"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="6bfa5-109">Registrando o provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="6bfa5-109">Registering the Service Provider</span></span>

<span data-ttu-id="6bfa5-110">Além de serem registrados como um objeto COM, um provedor de serviços deve ser registrado como um plug-in no Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6bfa5-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="6bfa5-111">Para se registrar, um provedor de serviços deve criar a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6bfa5-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="6bfa5-112">Nessa chave, < *seu nome de provedor de serviço* > é o nome da sua dll; por exemplo, o provedor de serviços de exemplo usa MsHDSP.</span><span class="sxs-lookup"><span data-stu-id="6bfa5-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="6bfa5-113">A chave ProgID deve ter um valor de cadeia de caracteres que corresponda ao CLSID do seu provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="6bfa5-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="6bfa5-114">Por exemplo, o provedor de serviços de exemplo tem o valor "MDServiceProviderHD. MDServiceProviderHD".</span><span class="sxs-lookup"><span data-stu-id="6bfa5-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="6bfa5-115">A implementação do provedor de serviço de exemplo DLLRegisterServer em MDSP. cpp adiciona essa chave do registro quando você registra a DLL do provedor de serviço de exemplo.</span><span class="sxs-lookup"><span data-stu-id="6bfa5-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bfa5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bfa5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bfa5-117">**Criando um provedor de serviços**</span><span class="sxs-lookup"><span data-stu-id="6bfa5-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




