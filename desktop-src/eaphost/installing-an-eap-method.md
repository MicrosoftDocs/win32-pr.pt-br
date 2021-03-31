---
title: Instalando um método EAP
description: Siga as instruções abaixo para instalar um método EAP implementado pelo usuário em um computador cliente que executa o EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640846"
---
# <a name="installing-an-eap-method"></a><span data-ttu-id="95b4d-103">Instalando um método EAP</span><span class="sxs-lookup"><span data-stu-id="95b4d-103">Installing an EAP Method</span></span>

<span data-ttu-id="95b4d-104">Siga as instruções abaixo para instalar um método EAP implementado pelo usuário em um computador cliente que executa o EAPHost.</span><span class="sxs-lookup"><span data-stu-id="95b4d-104">Follow the instructions below to install a user-implemented EAP method on a client computer running EAPHost.</span></span>

-   <span data-ttu-id="95b4d-105">Implemente [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DLLUNREGISTERSERVER**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) para a DLL do método EAP.</span><span class="sxs-lookup"><span data-stu-id="95b4d-105">Implement [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) for your EAP Method DLL.</span></span> <span data-ttu-id="95b4d-106">Essas funções adicionam e removem as chaves do registro apropriadas para o método EAP durante o processo de instalação e (desinstalação).</span><span class="sxs-lookup"><span data-stu-id="95b4d-106">These functions add and remove the appropriate registry keys for your EAP method during the installation and (uninstallation) process.</span></span>

    <span data-ttu-id="95b4d-107">Para obter informações sobre as chaves de registro específicas associadas à instalação de um método EAP, consulte o tópico [configuração do registro para métodos EAP](registry-keys-for-eap-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="95b4d-107">For information on the specific registry keys associated with the installation of an EAP method, see the [Registry Configuration for EAP Methods](registry-keys-for-eap-methods.md) topic.</span></span>

-   <span data-ttu-id="95b4d-108">Instale a DLL que contém a implementação do método EAP com o comando do console a seguir.</span><span class="sxs-lookup"><span data-stu-id="95b4d-108">Install the DLL that contains the EAP method implementation with the following console command.</span></span>

    <span data-ttu-id="95b4d-109"> *&lt; Nome &gt; da dll* regsvr32.exe</span><span class="sxs-lookup"><span data-stu-id="95b4d-109">**regsvr32.exe** *&lt;DLL name&gt;*</span></span>

    <span data-ttu-id="95b4d-110">Para desinstalar a DLL, use o seguinte comando de console:</span><span class="sxs-lookup"><span data-stu-id="95b4d-110">To uninstall the DLL, use the following console command:</span></span>

    <span data-ttu-id="95b4d-111">**regsvr32.exe** **/u** *&lt; nome &gt; da dll*</span><span class="sxs-lookup"><span data-stu-id="95b4d-111">**regsvr32.exe** **/u** *&lt;DLL name&gt;*</span></span>

-   <span data-ttu-id="95b4d-112">Reinicie o serviço EAPHost.</span><span class="sxs-lookup"><span data-stu-id="95b4d-112">Restart the EAPHost service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95b4d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95b4d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b4d-114">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="95b4d-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 