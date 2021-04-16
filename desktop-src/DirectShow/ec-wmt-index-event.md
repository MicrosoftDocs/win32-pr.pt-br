---
description: Enviado quando um aplicativo usa o filtro de gravador ASF do WM para indexar arquivos de vídeo do Windows Media.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782248"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (DShow. h)

Enviado quando um aplicativo usa o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) para indexar arquivos de vídeo do Windows Media.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Pode ser uma das seguintes mensagens **de \_ status WMT** .



| Valor                | Descrição              |
|----------------------|--------------------------|
| WMT \_ iniciado         | A indexação foi iniciada.      |
| WMT \_ fechado          | A indexação foi concluída.  |
| \_progresso do índice de WMT \_ | A indexação está em andamento. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *lParam1* for WMT \_ Closed ou WMT \_ iniciado, *lParam2* será zero. Se *lParam1* for WMT \_ index \_ Progress, *lParam2* será um **DWORD** que especifica o andamento atual como uma porcentagem do tamanho total do download.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




