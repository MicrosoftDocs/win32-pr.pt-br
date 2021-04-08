---
title: EC_WMT_INDEX_EVENT (SDK do Windows Media Format 11)
description: evento de índice do EC \_ WMT \_ \_
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK do Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- ASF (Advanced Systems Format), EC_WMT_INDEX_EVENT
- ASF (formato de sistemas avançados), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008695"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (SDK do Windows Media Format 11)

Enviado pelo Windows Media Format SDK quando um aplicativo usa o gravador ASF para indexar arquivos de vídeo do Windows Media.

Parâmetros

*lParam1*

Pode ser qualquer uma das seguintes mensagens **de \_ status WMT** .



| Mensagem              | Descrição                                     |
|----------------------|-------------------------------------------------|
| WMT \_ iniciado         | A indexação foi iniciada. *lParam2* é zero.          |
| WMT \_ fechado          | A indexação foi concluída. *lParam2* é zero. |
| \_progresso do índice de WMT \_ | A indexação está em andamento.                        |



 

*lParam2*

Se *lParam1* for WMT \_ Closed ou WMT \_ iniciado, *lParam2* será zero. Se *lParam1* for WMT \_ index \_ Progress, *lParam2* será um **DWORD** que expressa a quantidade de progresso como uma porcentagem do tamanho total do download.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência do QASF do DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 




