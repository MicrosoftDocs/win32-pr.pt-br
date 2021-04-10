---
title: Atualizando licenças
description: Atualizando licenças
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Armazenamentos online do Windows Media Player, atualizando licenças
- lojas online, atualizando licenças
- Digite 1 lojas online, atualizando licenças
- Lojas online do Windows Media Player, atualizando licenças
- lojas online, atualização de licenças
- tipo 1 lojas online, atualização de licença
- Atualizando licenças
- licenças, atualizando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293772"
---
# <a name="updating-licenses"></a><span data-ttu-id="af8f4-111">Atualizando licenças</span><span class="sxs-lookup"><span data-stu-id="af8f4-111">Updating Licenses</span></span>

<span data-ttu-id="af8f4-112">As lojas online podem fornecer conteúdo licenciado por um período de tempo específico ou até uma determinada data.</span><span class="sxs-lookup"><span data-stu-id="af8f4-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="af8f4-113">Isso seria normal para conteúdo de música entregue como parte de um contrato de serviço de assinatura.</span><span class="sxs-lookup"><span data-stu-id="af8f4-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="af8f4-114">Nesse caso, a loja online precisa de uma oportunidade para atualizar essas licenças antes que elas expirem, pressupondo, é claro, que o usuário tenha pago para renovar sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="af8f4-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="af8f4-115">(Se o usuário não tiver renovado a assinatura, as licenças podem simplesmente ser deixadas para expirar.)</span><span class="sxs-lookup"><span data-stu-id="af8f4-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="af8f4-116">O Windows Media Player consulta o plug-in do parceiro de conteúdo sobre a quantidade de aviso antecipado que o Player deve fornecer sobre uma licença que está prestes a expirar.</span><span class="sxs-lookup"><span data-stu-id="af8f4-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="af8f4-117">Ele faz isso chamando [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando a constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning por meio do parâmetro *bstrInfoName* .</span><span class="sxs-lookup"><span data-stu-id="af8f4-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="af8f4-118">Para alertar o plug-in sobre as licenças que estão prestes a expirar, o Windows Media Player chama [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span><span class="sxs-lookup"><span data-stu-id="af8f4-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="af8f4-119">Essa chamada usa parâmetros que fornecem detalhes sobre o arquivo que está sendo atualizado, como se o arquivo está no computador do usuário e o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="af8f4-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="af8f4-120">Se a licença estiver sendo atualizada como parte de uma operação de sincronização de dispositivo, o parâmetro *pReasonContext* fornecerá o nome cannonical do dispositivo</span><span class="sxs-lookup"><span data-stu-id="af8f4-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="af8f4-121">Quando o Windows Media Player chama **RefreshLicence**, ele passa um cookie que identifica a solicitação de atualização.</span><span class="sxs-lookup"><span data-stu-id="af8f4-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="af8f4-122">Quando o plug-in conclui o processamento da solicitação de atualização, ele notifica o Windows Media Player chamando [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando o cookie, a ID do item de mídia e um **HRESULT** que indica se a atualização foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="af8f4-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="af8f4-123">Os plug-ins da loja online também podem fazer a inspeção de licença e as atualizações como um processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="af8f4-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="af8f4-124">O Windows Media Player notifica o plug-in sobre os horários em que é permitido executar tarefas de processamento em segundo plano chamando [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span><span class="sxs-lookup"><span data-stu-id="af8f4-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="af8f4-125">Para sinalizar o plug-in para iniciar o processamento em segundo plano, o Player passa o valor de enumeração [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; para sinalizar o plug-in para interromper o processamento em segundo plano, o Player passa o valor wmpsnBackgroundProcessingEnd.</span><span class="sxs-lookup"><span data-stu-id="af8f4-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8f4-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af8f4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8f4-127">**Guia de programação para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="af8f4-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




