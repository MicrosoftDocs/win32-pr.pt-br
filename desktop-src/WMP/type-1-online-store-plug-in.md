---
title: Tipo 1 plug-in de loja online
description: Tipo 1 plug-in de loja online
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Lojas online do Windows Media Player, interface IWMPContentPartner
- lojas online, interface IWMPContentPartner
- Digite 1 lojas online, interface IWMPContentPartner
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, interface IWMPContentPartner
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, interface IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007248"
---
# <a name="type-1-online-store-plug-in"></a>Tipo 1 plug-in de loja online

Para aproveitar os recursos de integração de biblioteca, digite 1 provedores de loja online devem criar um plug-in que implemente a interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Essa interface fornece os métodos que o Windows Media Player chama para notificar a loja online sobre as atividades que estão ocorrendo no Player e recuperar informações específicas sobre o conteúdo da loja online, o catálogo ou a própria loja.

Depois que o Windows Media Player instancia o plug-in, o jogador chama [IWMPContentPartner:: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)e fornece um ponteiro para a interface **IWMPContentPartnerCallback** . Essa interface fornece ao armazenamento online uma maneira de fazer chamadas no Windows Media Player para fornecer informações de status ou para iniciar processos específicos, como baixar uma faixa de música.

O Windows Media Player e o plug-in são executados em processos separados. O plug-in é um servidor em processo que é executado na DLL padrão alternativa, dllhost.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Interface IWMPContentPartnerCallback**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




