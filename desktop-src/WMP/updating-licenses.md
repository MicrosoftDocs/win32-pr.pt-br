---
title: Atualizando licenças
description: Atualizando licenças
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player online, atualizando licenças
- lojas online, atualizando licenças
- tipo 1 lojas online, atualizando licenças
- Windows Media Player online, atualização de licença
- lojas online, atualização de licença
- tipo 1 lojas online, atualização de licença
- atualizando licenças
- licenças, atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182af125021af43b1a08695d00c194ec90c38a543d95123b093d30375e45e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117321"
---
# <a name="updating-licenses"></a>Atualizando licenças

As lojas online podem fornecer conteúdo licenciado por um período específico ou até uma determinada data. Isso seria normal para conteúdo de música entregue como parte de um contrato de serviço de assinatura. Nesse caso, a loja online precisa de uma oportunidade para atualizar essas licenças antes de expirarem, supondo, é claro, que o usuário tenha pago para renovar sua assinatura. (Se o usuário não tiver renovado a assinatura, as licenças poderão simplesmente ser deixadas para expirar.)

Windows Media Player consulta o plug-in do parceiro de conteúdo sobre quanto aviso antecipado o Player deve fornecer sobre uma licença que está prestes a expirar. Ele faz isso chamando [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando a constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning por meio do *parâmetro bstrInfoName.* Para alertar o plug-in sobre licenças que estão prestes a expirar, Windows Media Player chama [IWMPContentPartner::RefreshLicense.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense) Essa chamada aceita parâmetros que fornecem detalhes sobre o arquivo que está sendo atualizado, como se o arquivo está no computador do usuário e o caminho para o arquivo. Se a licença estiver sendo atualizada como parte de uma operação de sincronização de dispositivo, o parâmetro *pReasonContext* fornece o nome não criptografado do dispositivo

Quando Windows Media Player chama **RefreshLicence**, ele passa um cookie que identifica a solicitação de atualização. Quando o plug-in terminar de processar a solicitação de atualização, ele notifica o Windows Media Player chamando [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando o cookie, a ID do item de mídia e um **HRESULT** que indica se a atualização foi bem-sucedida.

Os plug-ins da loja online também podem fazer a inspeção de licença e as atualizações como um processo em segundo plano. Windows Media Player notifica o plug-in sobre horários em que é permitido executar tarefas de processamento em segundo plano chamando [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Para sinalizar o plug-in para iniciar o processamento em segundo plano, o Player passa o valor de enumeração [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; para sinalizar o plug-in para interromper o processamento em segundo plano, o Player passa o valor wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




