---
title: Identificadores de cliente
description: Identificadores de cliente
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Estrutura de Serviços de Texto (TSF), identificadores de cliente
- TSF (Estrutura de Serviços de Texto), identificadores de cliente
- serviços de texto, identificadores de cliente
- Aplicativos habilitados para TSF, identificadores de cliente
- identificadores de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953904"
---
# <a name="client-identifiers"></a>Identificadores de cliente

## <a name="applications"></a>Aplicativos

Um aplicativo obtém seu identificador de cliente chamando [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).

## <a name="text-services"></a>Serviços de Texto

Um serviço de texto obtém seu identificador de cliente quando o método [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) do serviço de texto é chamado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




