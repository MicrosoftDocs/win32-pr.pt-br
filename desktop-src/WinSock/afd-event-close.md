---
description: Evento de rastreamento de rede Winsock para operação de fechamento de soquete.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647146"
---
# <a name="afd_event_close-event"></a>Evento de fechamento de \_ evento de AFD \_

O evento de **\_ \_ fechamento de evento de AFD** é um evento de rastreamento de rede do Winsock para a operação de fechamento de soquete.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informações sobre este evento.

A tabela a seguir lista os possíveis valores para o parâmetro *EnterExit* :



| Valor                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | O início de uma solicitação do Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | A solicitação do Winsock foi concluída.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | O driver do Winsock AFD realizou uma ação interna (anulando uma conexão, por exemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | O driver TCP/IP fez com que esse evento ocorresse. Isso geralmente indica uma notificação de dados.<br/> |
| <dl> <dt>4</dt> </dl> | O driver do Winsock AFD fez com que esse evento ocorresse (definindo uma opção de soquete, por exemplo).<br/> |



 

</dd> <dt>

*Localidade* 
</dt> <dd>

Um campo privado usado internamente.

</dd> <dt>

*Processo* 
</dt> <dd>

O endereço [EPROCESS](/windows-hardware/drivers/kernel/eprocess) do processo que possui o soquete relacionado. Essa é uma estrutura opaca que serve como o objeto de processo para um processo. Para obter mais informações, consulte a documentação do Windows Driver Kit para a estrutura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Ponto de extremidade* 
</dt> <dd>

O \_ endereço do ponto de extremidade de AFD do soquete.

</dd> <dt>

*Status* 
</dt> <dd>

O código NTSTATUS para a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento de **\_ \_ fechamento de evento de AFD** é rastreado para uma operação de rede Winsock para fechar um soquete. O canal para esse evento é o Winsock-AFD. O nível desse evento é informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_descritor de evento**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

