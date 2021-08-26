---
description: O objeto de solicitação é criado usando COM CoCreateInstance e expõe uma interface, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto de solicitação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905886"
---
# <a name="request-object"></a>Objeto de solicitação

O objeto de solicitação é criado usando COM **CoCreateInstance** e expõe uma interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Essa interface expõe o método [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , que permite que um aplicativo TAPI 3 Use a telefonia assistida. A telefonia assistida fornece aplicativos habilitados para telefonia com um mecanismo simples para fazer chamadas telefônicas sem exigir que o desenvolvedor se torne totalmente compensante em telefonia.

Por exemplo, um aplicativo de planilha pode adicionar um botão "fazer chamada" usando a telefonia assistida sem implementar os controles mais elaborados disponíveis em um aplicativo TAPI completo.

Consulte a [visão geral de telefonia assistida](assisted-telephony-overview.md) para obter informações adicionais.

 

 



