---
title: Mensagem de WM_DDE_ACK (DDE. h)
description: A \_ mensagem de ACK DDE do WM \_ Notifica um aplicativo troca dinâmica de dados (DDE) do recebimento e do processamento das seguintes mensagens do WM \_ DDE enviar, do \_ WM \_ DDE \_ Execute, do WM DDE \_ \_ data, do WM \_ DDE \_ Advise, \_ do WM DDE UNADVISE, do WM \_ \_ DDE \_ INITIATE ou \_ \_ da solicitação DDE do WM (em alguns casos). Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Troca de dados de mensagem WM_DDE_ACK
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009288"
---
# <a name="wm_dde_ack-message"></a>\_Mensagem de ACK DDE do WM \_

A **mensagem \_ de \_ ACK DDE do WM** notifica um aplicativo troca dinâmica de dados (DDE) do recebimento e do processamento das seguintes mensagens: [**WM \_ DDE \_**](wm-dde-poke.md)enviar, [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md), [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md)ou a [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) (em alguns casos).

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ao responder ao [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md), esse parâmetro é um identificador para a janela do servidor que está enviando a mensagem.

Ao responder ao [**WM \_ DDE \_ Execute**](wm-dde-execute.md), esse parâmetro é um identificador para a janela do servidor que está postando a mensagem.

Ao responder a todas as outras mensagens, esse parâmetro é um identificador para a janela do cliente ou do servidor que está postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Ao responder ao [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md), a palavra de ordem inferior contém um Atom que identifica o aplicativo de resposta. A palavra de ordem superior contém um átomo que identifica o tópico para o qual uma conversa está sendo estabelecida.

Ao responder ao [**WM \_ DDE \_ Execute**](wm-dde-execute.md), a palavra de ordem inferior Especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta. A palavra de ordem superior é um identificador para um objeto de memória global que contém a cadeia de caracteres de comando que foi recebida na mensagem de **\_ \_ execução de DDE do WM** .

Ao responder a todas as outras mensagens, a palavra de ordem inferior Especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta. A palavra de ordem superior contém um átomo global que identifica o nome do item de dados para o qual a resposta é enviada.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Lançamento

Exceto em resposta à mensagem [**de \_ \_ início do WM DDE**](wm-dde-initiate.md) , o aplicativo envia a mensagem de **ACK do WM \_ DDE \_** chamando a função de postagem, não chamando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . [](/windows/desktop/api/winuser/nf-winuser-postmessagea) Ao responder ao **WM \_ DDE \_ Iniciar**, o aplicativo envia a mensagem de **\_ \_ ACK DDE do WM** chamando **SendMessage**. Nesse caso, nem o átomo do nome do aplicativo nem o Atom do nome do tópico devem ser **nulos** (mesmo que a mensagem de **início do WM \_ DDE \_** especifique os átomos **nulos** ).

Ao confirmar qualquer mensagem com um átomo de acompanhamento, a postagem de aplicativo do **WM \_ DDE \_ ACK** pode reutilizar o Atom que acompanha a mensagem original ou pode excluí-la e criar uma nova.

Ao confirmar que o [**WM \_ DDE \_ é executado**](wm-dde-execute.md), o aplicativo que publica o **WM \_ DDE \_ ACK** deve reutilizar o objeto de memória global identificado na mensagem de **\_ \_ execução DDE do WM** original.

Todas as mensagens de **\_ \_ ACK DDE do WM** lançadas devem criar ou reutilizar o parâmetro *lParam* chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se um aplicativo tiver iniciado o encerramento de uma conversa postando [**a \_ \_ Encerração do WM DDE**](wm-dde-terminate.md) e estiver aguardando a confirmação, o aplicativo em espera não deverá reconhecer (positiva ou negativamente) todas as mensagens subsequentes enviadas pelo outro aplicativo. O aplicativo em espera deve excluir todos os átomos ou objetos de memória compartilhada recebidos nessas mensagens intervenientes. Os objetos de memória não devem ser liberados se o sinalizador **fRelease** estiver definido como **false** nas mensagens [**de \_ \_ dados**](wm-dde-data.md) DDE do WM e do WM DDE [**\_ \_**](wm-dde-poke.md) .

### <a name="receiving"></a>Recebimento

O aplicativo que recebe uma mensagem de **\_ \_ ACK DDE do WM** deve excluir todos os átomos que acompanham a mensagem. Se o aplicativo receber uma **\_ \_ confirmação de DDE do WM** em resposta a uma mensagem com um objeto de memória global que o acompanha e o objeto tiver sido enviado com os sinalizadores **fRelease** definidos como **false**, o aplicativo será responsável por excluir o objeto.

Se o aplicativo receber uma mensagem **de \_ \_ ACK DDE do WM** negativa postada em resposta a uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) , o aplicativo deverá excluir o objeto de memória global Postado com a mensagem de **\_ \_ aviso DDE do WM** original. Se o aplicativo receber uma mensagem **de \_ \_ ACK DDE do WM** negativa postada em resposta a uma mensagem de [**\_ \_ execução**](wm-dde-execute.md) do WM DDE [**\_ \_ Data**](wm-dde-data.md), do [**WM \_ DDE \_**](wm-dde-poke.md)ou do WM DDE, o aplicativo deverá excluir o objeto de memória global Postado com os **\_ \_ dados do WM DDE** original, o **WM \_ DDE \_** enviar ou a mensagem de **\_ \_ execução DDE do WM** .

O aplicativo que recebe uma mensagem **de \_ \_ ACK DDE do WM** lançada deve liberar o parâmetro *lParam* usando a função [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**\_aviso de DDE do WM \_**](wm-dde-advise.md)
</dt> <dt>

[**\_dados DDE do WM \_**](wm-dde-data.md)
</dt> <dt>

[**\_execução de DDE do WM \_**](wm-dde-execute.md)
</dt> <dt>

[**início do WM \_ DDE \_**](wm-dde-initiate.md)
</dt> <dt>

[**o WM \_ DDE. \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitação de DDE do WM \_**](wm-dde-request.md)
</dt> <dt>

[**fim do WM \_ DDE \_**](wm-dde-terminate.md)
</dt> <dt>

[**\_aviso de DDE do WM \_**](wm-dde-unadvise.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

