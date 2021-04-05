---
title: Mensagem de WM_DDE_ADVISE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta a mensagem de aviso de DDE do WM \_ \_ em um aplicativo de servidor DDE para solicitar que o servidor forneça uma atualização para um item de dados sempre que o item for alterado.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Troca de dados de mensagem WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085482"
---
# <a name="wm_dde_advise-message"></a>Mensagem de aviso de \_ DDE do WM \_

Um aplicativo cliente troca dinâmica de dados (DDE) posta a mensagem de **\_ \_ aviso de DDE do WM** em um aplicativo de servidor DDE para solicitar que o servidor forneça uma atualização para um item de dados sempre que o item for alterado.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) que especifica como os dados serão enviados.

A palavra de ordem superior contém um Atom que identifica o item de dados solicitado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se um aplicativo cliente oferecer suporte a mais de um formato de área de transferência para um único tópico e item, ele poderá postar várias mensagens de **\_ \_ aviso de DDE do WM** para o tópico e o item, especificando um formato de área de transferência diferente com cada mensagem. Observe que um servidor pode dar suporte a vários formatos somente para links de dados dinâmicos, não para links de dados quentes.

### <a name="posting"></a>Lançamento

O aplicativo cliente posta a mensagem de **\_ \_ aviso de DDE do WM** chamando a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , não a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

O aplicativo cliente aloca o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Ele aloca o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

O aplicativo cliente deve criar ou reutilizar o parâmetro *lParam* do **\_ \_ visor de comunicação do WM** chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se o aplicativo receptor (servidor) responder com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa, o aplicativo de lançamento deverá excluir o objeto.

O **sinalizador fRelease** não é usado em mensagens de **\_ \_ aviso de DDE do WM** , mas seu comportamento de liberação de dados é semelhante ao do [**WM \_ DDE \_ Data**](wm-dde-data.md) e ao [**WM \_ DDE \_**](wm-dde-poke.md) fazer mensagens em que **fRelease** é **verdadeiro**.

### <a name="receiving"></a>Recebimento

O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente. Ao lançar o aplicativo de **\_ \_ confirmação de DDE do WM**, ele pode reutilizar o Atom ou excluí-lo e criar um novo. Se a mensagem de **\_ \_ ACK DDE do WM** for positiva, o aplicativo deverá excluir o objeto de memória global; caso contrário, o aplicativo não deverá excluir o objeto.

O servidor deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**o WM \_ DDE. \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitação de DDE do WM \_**](wm-dde-request.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

