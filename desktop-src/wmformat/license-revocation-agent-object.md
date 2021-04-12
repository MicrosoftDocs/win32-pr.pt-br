---
title: Objeto do agente de revogação de licença
description: Objeto do agente de revogação de licença
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- SDK do Windows Media Format, objetos do agente de revogação de licença
- ASF (Advanced Systems Format), objetos de agente de revogação de licença
- ASF (formato de sistemas avançados), objetos de agente de revogação de licença
- objetos, objetos do agente de revogação de licença
- revogação de licença, objetos do agente de revogação de licença
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365537"
---
# <a name="license-revocation-agent-object"></a>Objeto do agente de revogação de licença

O objeto do agente de revogação de licença gerencia o lado do cliente da revogação de licença. A revogação de licenças é o processo pelo qual um servidor de licença pode remover licenças do repositório de licenças no computador cliente. O processo envolve a passagem de várias mensagens entre o aplicativo cliente e o servidor de licença. Os métodos expostos neste objeto processam e geram essas mensagens.

O objeto do agente de revogação de licença é criado pela função [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , que define um ponteiro para uma interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) . **IUnknown** e **IWMLicenseRevocationAgent** são as únicas interfaces suportadas por este objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> </dl>

 

 




