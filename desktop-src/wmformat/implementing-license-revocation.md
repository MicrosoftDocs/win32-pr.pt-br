---
title: Implementando a revogação de licenças
description: Implementando a revogação de licenças
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- SDK do Windows Media Format, implementando a revogação de licença
- SDK do Windows Media Format, revogação de licença
- SDK do Windows Media Format, revogação de licenças
- ASF (Advanced Systems Format), implementando a revogação de licenças
- ASF (formato de sistemas avançados), implementando a revogação de licenças
- ASF (Advanced Systems Format), revogação de licença
- ASF (formato de sistemas avançados), revogação de licença
- ASF (Advanced Systems Format), revogação de licenças
- ASF (formato de sistemas avançados), revogação de licenças
- DRM (gerenciamento de direitos digitais), implementando a revogação de licenças
- DRM (gerenciamento de direitos digitais), implementando a revogação de licenças
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licenças
- DRM (gerenciamento de direitos digitais), revogação de licenças
- revogação de licença, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640163"
---
# <a name="implementing-license-revocation"></a>Implementando a revogação de licenças

O SDK do Windows Media Rights Manager 10 inclui um recurso chamado revogação de licenças. Esse recurso permite que os servidores de licenças solicitem que as licenças sejam removidas do computador cliente. O Windows Media Format SDK fornece métodos que processam mensagens de revogação e removem as licenças do armazenamento de licença local.

O processo de revogação de licença é iniciado por um serviço fornecido pelo emissor da licença. Seu aplicativo pode hospedar esse serviço ou pode ser um aplicativo Web. Em ambos os casos, seu aplicativo deve ser capaz de receber um desafio de licença criado pelo serviço.

Para remover licenças do repositório de licenças, execute as seguintes etapas:

1.  Após receber um desafio de licença do emissor da licença, chame a função [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) para criar um objeto do agente de revogação de licença e obter um ponteiro para a interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .
2.  Chame o método [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) para gerar a resposta de desafio.
3.  Envie a resposta de desafio de volta para o componente de serviço de licença do qual você recebeu o desafio.
4.  O componente de serviço de licença envia um LRB (blob de revogação de licença assinada) para seu aplicativo. Quando você o receber, chame o método [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) . O **ProcessLRB** cria uma mensagem de confirmação que você deve enviar de volta ao serviço de licença para verificar se as licenças foram removidas.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




