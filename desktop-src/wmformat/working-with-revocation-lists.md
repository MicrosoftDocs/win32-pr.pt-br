---
title: Trabalhando com listas de revogação
description: Trabalhando com listas de revogação
ms.assetid: 4463abb5-f48f-484f-b837-512313572c0a
keywords:
- SDK do Windows Media Format, listas de revogação
- ASF (Advanced Systems Format), listas de revogação
- ASF (formato de sistemas avançados), listas de revogação
- listas de revogação
- DRM (gerenciamento de direitos digitais), listas de revogação
- DRM (gerenciamento de direitos digitais), listas de revogação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f4eca82dd82c9225406a85034ff2a6df227fce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498974"
---
# <a name="working-with-revocation-lists"></a><span data-ttu-id="52bf2-109">Trabalhando com listas de revogação</span><span class="sxs-lookup"><span data-stu-id="52bf2-109">Working with Revocation Lists</span></span>

<span data-ttu-id="52bf2-110">Para responder a violações de segurança e para garantir que os aplicativos do Player conhecidos como rompidos ou comprometidos não possam reproduzir ou usar arquivos protegidos, cada licença emitida conterá uma lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="52bf2-110">To respond to security breaches and to ensure that player applications known to be broken or compromised cannot play or use protected files, each license that is issued contains a revocation list.</span></span> <span data-ttu-id="52bf2-111">Uma lista de revogação contém os certificados de aplicativo de todos os aplicativos do Player conhecidos como danificados ou corrompidos.</span><span class="sxs-lookup"><span data-stu-id="52bf2-111">A revocation list contains the application certificates of all those player applications known to be broken or corrupted.</span></span> <span data-ttu-id="52bf2-112">Quando uma nova licença é recebida, o componente DRM do aplicativo de Player verifica se há uma lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="52bf2-112">When a new license is received, the DRM component of the player application checks for a revocation list.</span></span> <span data-ttu-id="52bf2-113">Se for encontrado um que seja mais recente do que o atualmente no computador, a lista mais recente será armazenada.</span><span class="sxs-lookup"><span data-stu-id="52bf2-113">If one is found that is newer than the one currently on the computer, the newer list is stored.</span></span> <span data-ttu-id="52bf2-114">Na próxima vez que o consumidor reproduzir um arquivo ASF protegido, o componente DRM compara o aplicativo de Player com a lista de revogação.</span><span class="sxs-lookup"><span data-stu-id="52bf2-114">The next time the consumer plays a protected ASF file, the DRM component compares the player application to the revocation list.</span></span> <span data-ttu-id="52bf2-115">Se o aplicativo de player for revogado, o componente DRM enviará uma mensagem de erro ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="52bf2-115">If the player application is revoked, the DRM component sends an error message to the application.</span></span>

<span data-ttu-id="52bf2-116">Os aplicativos do Player podem receber uma mensagem de erro de revogação nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="52bf2-116">Player applications can receive a revocation error message in the following scenarios:</span></span>

-   <span data-ttu-id="52bf2-117">A mensagem de erro é recebida depois que o aplicativo chama o método [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) para um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="52bf2-117">The error message is received after the application calls the [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) method for a protected file.</span></span> <span data-ttu-id="52bf2-118">A chamada falha com o código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revogado, que é fornecido para a função de retorno de chamada **OnStatus** com o \_ status de licença de aquisição WMT \_ .</span><span class="sxs-lookup"><span data-stu-id="52bf2-118">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the **OnStatus** callback function with WMT\_ACQUIRE\_LICENSE status.</span></span> <span data-ttu-id="52bf2-119">Se esse código **HRESULT** for ignorado, os erros continuarão ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="52bf2-119">If this **HRESULT** code is ignored, errors will continue to occur.</span></span>
-   <span data-ttu-id="52bf2-120">A mensagem de erro é recebida quando o aplicativo cria o leitor habilitado para DRM e chama o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) para um arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="52bf2-120">The error message is received when the application creates the DRM-enabled reader and calls the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method for a protected file.</span></span> <span data-ttu-id="52bf2-121">A chamada falha com o código **HRESULT** NS \_ E \_ DRM \_ APPCERT \_ revogado, que é fornecido para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) com o \_ status aberto WMT.</span><span class="sxs-lookup"><span data-stu-id="52bf2-121">The call fails with the **HRESULT** code NS\_E\_DRM\_APPCERT\_REVOKED, which is supplied to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method with WMT\_OPENED status.</span></span> <span data-ttu-id="52bf2-122">Quando um aplicativo de Player recebe essa mensagem de erro, o aplicativo deve notificar os usuários finais e fornecer uma maneira para que eles restaurem a funcionalidade para o Player.</span><span class="sxs-lookup"><span data-stu-id="52bf2-122">When a player application receives this error message, the application should notify end users and provide a way for them to restore functionality to their player.</span></span> <span data-ttu-id="52bf2-123">Por exemplo, o aplicativo pode abrir uma URL onde os usuários finais podem baixar uma atualização para o aplicativo comprometido.</span><span class="sxs-lookup"><span data-stu-id="52bf2-123">For example, the application can open a URL where end users can download an upgrade for the compromised application.</span></span>

<span data-ttu-id="52bf2-124">**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="52bf2-124">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52bf2-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52bf2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52bf2-126">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="52bf2-126">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="52bf2-127">**Lidando com eventos de aquisição de licença**</span><span class="sxs-lookup"><span data-stu-id="52bf2-127">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> </dl>

 

 




