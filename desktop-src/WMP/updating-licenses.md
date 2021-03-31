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
# <a name="updating-licenses"></a>Atualizando licenças

As lojas online podem fornecer conteúdo licenciado por um período de tempo específico ou até uma determinada data. Isso seria normal para conteúdo de música entregue como parte de um contrato de serviço de assinatura. Nesse caso, a loja online precisa de uma oportunidade para atualizar essas licenças antes que elas expirem, pressupondo, é claro, que o usuário tenha pago para renovar sua assinatura. (Se o usuário não tiver renovado a assinatura, as licenças podem simplesmente ser deixadas para expirar.)

O Windows Media Player consulta o plug-in do parceiro de conteúdo sobre a quantidade de aviso antecipado que o Player deve fornecer sobre uma licença que está prestes a expirar. Ele faz isso chamando [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando a constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning por meio do parâmetro *bstrInfoName* . Para alertar o plug-in sobre as licenças que estão prestes a expirar, o Windows Media Player chama [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Essa chamada usa parâmetros que fornecem detalhes sobre o arquivo que está sendo atualizado, como se o arquivo está no computador do usuário e o caminho para o arquivo. Se a licença estiver sendo atualizada como parte de uma operação de sincronização de dispositivo, o parâmetro *pReasonContext* fornecerá o nome cannonical do dispositivo

Quando o Windows Media Player chama **RefreshLicence**, ele passa um cookie que identifica a solicitação de atualização. Quando o plug-in conclui o processamento da solicitação de atualização, ele notifica o Windows Media Player chamando [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando o cookie, a ID do item de mídia e um **HRESULT** que indica se a atualização foi bem-sucedida.

Os plug-ins da loja online também podem fazer a inspeção de licença e as atualizações como um processo em segundo plano. O Windows Media Player notifica o plug-in sobre os horários em que é permitido executar tarefas de processamento em segundo plano chamando [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Para sinalizar o plug-in para iniciar o processamento em segundo plano, o Player passa o valor de enumeração [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; para sinalizar o plug-in para interromper o processamento em segundo plano, o Player passa o valor wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




