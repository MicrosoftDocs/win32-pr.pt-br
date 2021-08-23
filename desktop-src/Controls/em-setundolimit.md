---
title: Mensagem de EM_SETUNDOLIMIT (RichEdit. h)
description: Define o número máximo de ações que podem ser armazenadas na fila de desfazer de um controle de edição rico.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- controles de Windows de mensagem de EM_SETUNDOLIMIT
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697516"
---
# <a name="em_setundolimit-message"></a>\_Mensagem em SETUNDOLIMIT

Define o número máximo de ações que podem ser armazenadas na fila de desfazer de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o número máximo de ações que podem ser armazenadas na fila de desfazer.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o novo número máximo de ações de desfazer para o controle de edição rico. Esse valor pode ser menor que *wParam* se a memória for limitada.

## <a name="remarks"></a>Comentários

Por padrão, o número máximo de ações na fila de desfazer é de 100. Se você aumentar esse número, deverá haver memória suficiente disponível para acomodar o novo número. Para obter um melhor desempenho, defina o limite para o menor valor possível.

Definir o limite como zero desabilita o recurso de **desfazer** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ refazer**](em-canredo.md)
</dt> <dt>

[**em \_ refazer**](em-getredoname.md)
</dt> <dt>

[**em \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**em \_ refazer**](em-redo.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





