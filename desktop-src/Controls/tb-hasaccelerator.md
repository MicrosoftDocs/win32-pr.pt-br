---
title: Mensagem de TB_HASACCELERATOR (commctrl. h)
description: Recupera uma contagem de botões da barra de ferramentas que têm o caractere de acelerador especificado.
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- controles de Windows de mensagem de TB_HASACCELERATOR
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420f06e71c6920c266c96d8b2580549fa0eaace2bd3abdd37524502d4039aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078280"
---
# <a name="tb_hasaccelerator-message"></a>TB de \_ mensagem HASACCELERATOR

\[Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Recupera uma contagem de botões da barra de ferramentas que têm o caractere de acelerador especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **WCHAR** que representa o caractere do acelerador de entrada a ser testado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um **int** que recebe o número de botões que têm o caractere de acelerador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="security-considerations"></a>Considerações de segurança

O uso dessa mensagem pode comprometer a segurança do seu programa.

## <a name="remarks"></a>Comentários

Primeiro, o sistema consulta todos os botões da barra de ferramentas para os aceleradores correspondentes. Se nenhuma correspondência for encontrada, o sistema enviará a notificação [tbn \_ MAPACCELERATOR](tbn-mapaccelerator.md) para a janela pai, solicitando o índice do botão que tem o caractere de acelerador especificado. Se o pai fornecer um índice, a contagem será definida como 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





