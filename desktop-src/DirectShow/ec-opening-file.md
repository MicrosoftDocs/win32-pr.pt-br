---
description: O grafo está abrindo um arquivo ou concluiu a abertura de um arquivo.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 436a48a90640577504871dfe835d6c81c398680ae070065189cb4031493e7fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079116"
---
# <a name="ec_opening_file"></a>ARQUIVO DE \_ ABERTURA \_ DE EC

O grafo está abrindo um arquivo ou concluiu a abertura de um arquivo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

**TRUE** se o grafo estiver começando a abrir um arquivo ou **FALSE** se o grafo não estiver mais abrindo o arquivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Um filtro poderá enviar esse evento se ele gastar um tempo significativo abrindo um arquivo. (Por exemplo, o arquivo pode estar localizado em uma rede.) O aplicativo pode usar esse evento para ajustar sua interface do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




