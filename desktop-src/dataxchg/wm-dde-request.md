---
title: Mensagem de WM_DDE_REQUEST (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma \_ mensagem de solicitação de DDE do WM \_ em um aplicativo de servidor DDE para solicitar o valor de um item de dados. Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Troca de dados de mensagem WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644546"
---
# <a name="wm_dde_request-message"></a>Mensagem de solicitação de \_ DDE do WM \_

Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ solicitação de DDE do WM** em um aplicativo de servidor DDE para solicitar o valor de um item de dados.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está enviando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica um formato de área de transferência padrão ou registrado.

A palavra de ordem superior contém um Atom que identifica o item de dados solicitado do servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Lançamento

O aplicativo cliente aloca o Atom chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

### <a name="receiving"></a>Recebimento

Se o aplicativo receptor (servidor) puder atender à solicitação, ele responderá com uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) contendo os dados solicitados. Caso contrário, ele responde com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.

Ao responder com uma mensagem do [**WM DDE \_ \_ Data**](wm-dde-data.md) ou do [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , o aplicativo de servidor pode reutilizar o Atom ou pode excluir o Atom e criar um novo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK de DDE do WM \_**](wm-dde-ack.md)
</dt> <dt>

[**\_dados DDE do WM \_**](wm-dde-data.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

