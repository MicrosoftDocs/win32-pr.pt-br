---
description: CPL_INQUIRE mensagem – enviada para a função CPlApplet de um aplicativo Painel de Controle para solicitar informações sobre uma caixa de diálogo compatível com o aplicativo.
title: CPL_INQUIRE mensagem (Cpl.h)
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
ms.openlocfilehash: 5998e26eab79d3e5f0b9e3628614e1cc2ecbfb7040e866a898a09ad54fa49f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710716"
---
# <a name="cpl_inquire-message"></a>Mensagem CPL \_ INQUIRE

Enviado para a [**função CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um Painel de Controle para solicitar informações sobre uma caixa de diálogo compatível com o aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uAppNum* 
</dt> <dd>

O número da caixa de diálogo. Esse número deve estar no intervalo de zero a um menor que o valor retornado em resposta à mensagem [**\_ GETCOUNT**](cpl-getcount.md) da CPL (CPL \_ GETCOUNT – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

O endereço de uma [**estrutura CPLINFO.**](/windows/win32/api/cpl/ns-cpl-cplinfo) O aplicativo deve preencher essa estrutura com identificadores de recurso para o ícone, o nome curto, a descrição e qualquer valor definido pelo usuário associado à caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a [**função CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processa essa mensagem com êxito, ela deve retornar zero.

## <a name="remarks"></a>Comentários

O Painel de Controle envia a mensagem **CPL \_ INQUIRE** uma vez para cada caixa de diálogo com suporte em seu aplicativo. O Painel de Controle também envia uma [**mensagem CPL \_ NEWINQUIRE para**](cpl-newinquire.md) cada caixa de diálogo. Essas mensagens são enviadas imediatamente após a [**mensagem \_ GETCOUNT da CPL.**](cpl-getcount.md) No entanto, o sistema não garante a ordem na qual as **mensagens CPL \_ INQUIRE** e **CPL \_ NEWINQUIRE** são enviadas.

Você pode executar a inicialização para a caixa de diálogo quando receber **CPL \_ INQUIRE**. Se você precisa alocar memória, faça isso em resposta à mensagem [**\_ CPL INIT.**](cpl-init.md)

A [**mensagem CPL \_ NEWINQUIRE**](cpl-newinquire.md) retorna informações em um formulário que o sistema não pode armazenar em cache. Por esse motivo, a [**maioria das funções CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve processar **CPL \_ INQUIRE** e ignorar **CPL \_ NEWINQUIRE**.

Os únicos aplicativos que devem usar [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) são aqueles que precisam alterar seu ícone ou exibir cadeias de caracteres com base no estado do computador. Nesse caso, o manipulador **CPL \_ INQUIRE** deve especificar o valor DE RES DINÂMICO DA CPL para os membros \_ \_ **idIcon**, **idName** ou **idInfo** da estrutura [**CPLINFO,**](/windows/win32/api/cpl/ns-cpl-cplinfo) em vez de especificar um identificador de recurso válido. Isso faz com que o Painel de Controle envie a mensagem **CPL \_ NEWINQUIRE** sempre que precisar do ícone e das cadeias de caracteres de exibição, permitindo que você especifique informações com base no estado atual do computador. Isso é significativamente mais lento do que usar informações armazenadas em cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



 

 
