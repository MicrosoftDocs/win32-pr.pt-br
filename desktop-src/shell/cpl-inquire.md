---
description: CPL_INQUIRE mensagem enviada à função CPlApplet de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104464"
---
# <a name="cpl_inquire-message"></a>CPL \_ mensagem de consulta

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo. Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

O endereço de uma estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . O aplicativo deve preencher essa estrutura com identificadores de recurso para o ícone, nome curto, descrição e qualquer valor definido pelo usuário associado à caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.

## <a name="remarks"></a>Comentários

O painel de controle envia a mensagem de **\_ consulta de CPL** uma vez para cada caixa de diálogo com suporte do seu aplicativo. O painel de controle também envia uma mensagem [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) para cada caixa de diálogo. Essas mensagens são enviadas imediatamente após a mensagem de [**\_ sqlcount do CPL**](cpl-getcount.md) . No entanto, o sistema não garante a ordem na qual as mensagens **CPL \_ inquire** e **CPL \_ NEWINQUIRE** são enviadas.

Você pode executar a inicialização para a caixa de diálogo ao receber a **CPL de \_ consulta**. Se você precisar alocar memória, faça isso em resposta à mensagem [**CPL de \_ inicialização**](cpl-init.md) .

A mensagem [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) retorna informações em um formato que o sistema não pode armazenar em cache. Por esse motivo, a maioria das funções [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve processar a **CPL de \_ consulta** e ignorar o **CPL \_ NEWINQUIRE**.

Os únicos aplicativos que devem usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) são aqueles que precisam alterar seu ícone ou cadeias de caracteres de exibição com base no estado do computador. Nesse caso, o manipulador **de \_ consultas de CPL** deve especificar o \_ valor de res dinâmico CPL \_ para os membros **idIcon**, **idname** ou **IdInfo** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , em vez de especificar um identificador de recurso válido. Isso faz com que o painel de controle envie a mensagem **CPL \_ NEWINQUIRE** sempre que precisa do ícone e cadeias de caracteres de exibição, permitindo que você especifique informações com base no estado atual do computador. Isso é significativamente mais lento do que usar informações armazenadas em cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
