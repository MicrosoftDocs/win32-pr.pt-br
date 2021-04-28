---
description: CPL_NEWINQUIRE mensagem enviada à função CPlApplet de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.
title: Mensagem de CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104434"
---
# <a name="cpl_newinquire-message"></a>CPL \_ mensagem NEWINQUIRE

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle para solicitar informações sobre uma caixa de diálogo à qual o aplicativo dá suporte.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo. Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**CPL \_ GetCount**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

O endereço de uma estrutura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . O aplicativo do painel de controle deve preencher essa estrutura com informações sobre a caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.

## <a name="remarks"></a>Comentários

Para melhorar o desempenho, a maioria dos aplicativos deve ignorar o **CPL \_ NEWINQUIRE** e processar a mensagem de [**\_ consulta do CPL**](cpl-inquire.md) .

O painel de controle envia a mensagem **CPL \_ NEWINQUIRE** uma vez para cada caixa de diálogo com suporte do seu aplicativo. O painel de controle também envia uma mensagem de [**\_ consulta de CPL**](cpl-inquire.md) para cada caixa de diálogo. Essas mensagens são enviadas imediatamente após a mensagem de [**\_ sqlcount do CPL**](cpl-getcount.md) . No entanto, o sistema não garante a ordem na qual as mensagens **CPL \_ inquire** e **CPL \_ NEWINQUIRE** são enviadas.

Você pode executar a inicialização para a caixa de diálogo ao receber a [**CPL de \_ consulta**](cpl-inquire.md). Se você precisar alocar memória, faça isso em resposta à mensagem [**CPL de \_ inicialização**](cpl-init.md) .

[**CPL \_ A consulta**](cpl-inquire.md) é a mensagem preferida. Isso ocorre porque o **CPL \_ NEWINQUIRE** retorna informações em um formato que o sistema não pode armazenar em cache. Consequentemente, os aplicativos que process **CPL \_ NEWINQUIRE** devem ser carregados cada vez que o painel de controle precisar das informações, resultando em uma redução significativa no desempenho.

Os únicos aplicativos que devem usar **CPL \_ NEWINQUIRE** são aqueles que precisam alterar seu ícone ou cadeias de caracteres de exibição com base no estado do computador. Nesse caso, o manipulador [**de \_ consultas de CPL**](cpl-inquire.md) deve especificar o \_ valor de res dinâmico CPL \_ para os membros **idIcon**, **idname** ou **IdInfo** da estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , em vez de especificar um identificador de recurso válido. Isso faz com que o painel de controle envie a mensagem **CPL \_ NEWINQUIRE** sempre que precisa do ícone e cadeias de caracteres de exibição, permitindo que você especifique informações com base no estado atual do computador. É claro que isso é significativamente mais lento do que o uso de informações armazenadas em cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
