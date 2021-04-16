---
description: O objeto de solicitação é criado usando COM CoCreateInstance e expõe uma interface, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Objeto de solicitação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759042"
---
# <a name="request-object"></a>Objeto de solicitação

O objeto de solicitação é criado usando COM **CoCreateInstance** e expõe uma interface, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Essa interface expõe o método [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , que permite que um aplicativo TAPI 3 Use a telefonia assistida. A telefonia assistida fornece aplicativos habilitados para telefonia com um mecanismo simples para fazer chamadas telefônicas sem exigir que o desenvolvedor se torne totalmente compensante em telefonia.

Por exemplo, um aplicativo de planilha pode adicionar um botão "fazer chamada" usando a telefonia assistida sem implementar os controles mais elaborados disponíveis em um aplicativo TAPI completo.

Consulte a [visão geral de telefonia assistida](assisted-telephony-overview.md) para obter informações adicionais.

 

 



