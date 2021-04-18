---
description: Notifica o aplicativo sobre o progresso ao abrir um arquivo de rede.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780634"
---
# <a name="ec_loadstatus"></a>loadstatus do EC \_

Notifica o aplicativo sobre o progresso ao abrir um arquivo de rede.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Código de status. Consulte Observações.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

O filtro de [leitor ASF do WM](wm-asf-reader-filter.md) e o filtro de [origem do Windows Media](windows-media-source-filter.md) herdado enviam esse evento. O primeiro parâmetro de evento tem um dos valores a seguir.



| Valor                        | Descrição                                    |
|------------------------------|------------------------------------------------|
| \_loadstatus \_ encerrado       | O filtro de origem fechou o arquivo.         |
| \_conexão do LOADstatus \_   | O filtro de origem está se conectando ao servidor. |
| \_LOADINGDESCR LOADstatus \_ | Não usado.                                      |
| \_LOADINGMCAST LOADstatus \_ | Não usado                                       |
| \_loadstatus \_ localizando     | O filtro de origem está localizando os dados solicitados.  |
| \_loadstatus \_ aberto         | O filtro de origem abriu o arquivo.         |
| \_abertura de LOADSTATUS am \_      | O filtro de origem está abrindo o arquivo.         |



 

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

 

 




