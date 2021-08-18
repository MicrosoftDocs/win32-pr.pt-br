---
title: Criando o plug-in para uma loja online tipo 1
description: Criando o plug-in para uma loja online tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player lojas online, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Windows Media Player lojas online, criando plug-ins
- lojas online, criando plug-ins
- Digite 1 lojas online, criando plug-ins
- Windows Media Player lojas online, interface IWMPContentPartner
- lojas online, interface IWMPContentPartner
- Digite 1 lojas online, interface IWMPContentPartner
- plug-ins, Windows Media Player lojas online
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, interface IWMPContentPartner
- plug-ins, compilando
- plug-ins Windows Media Player, tipo 1 lojas online
- plug-ins Windows Media Player, lojas online
- Windows Media Player plug-ins, Windows Media Player lojas online
- plug-ins Windows Media Player, interface IWMPContentPartner
- plug-ins Windows Media Player, compilando
- IWMPContentPartner
- Criando plug-ins, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fdc5b01a0a8ec526af22e6be90c562524536cdb30b37bd03eb40132af0be49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997846"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Criando o plug-in para uma loja online tipo 1

Um repositório online tipo 1 deve fornecer um plug-in que implementa a interface [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . O plug-in é executado em um processo separado do Windows Media Player.

As etapas para criar um plug-in que executa fora do processo são as seguintes:

1.  Escreva seu plug-in como se fosse um servidor COM em processo.
2.  Crie uma entrada de registro **DllSurrogate** no computador do usuário. A entrada **DllSurrogate** informa ao tempo de execução com que seu plug-in deve ser criado em uma instância da dll padrão, alternativa, dllhost.exe.

Para obter informações detalhadas sobre como registrar seu plug-in, consulte [chaves e entradas do registro para um repositório online tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

Você não precisa criar nenhum código de proxy ou stub para seu plug-in. Todo o suporte a marshaling é fornecido pelo Windows Media Player.

Você pode usar o assistente de plug-in da loja online para criar rapidamente um plug-in que serve como ponto de partida. Para obter mais informações, consulte [instalando o assistente de plug-in da loja online](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




