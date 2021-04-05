---
title: Mensagem de EM_SETUNDOLIMIT (RichEdit. h)
description: Define o número máximo de ações que podem ser armazenadas na fila de desfazer de um controle de edição rico.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Controles de EM_SETUNDOLIMIT de mensagens do Windows
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
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918613"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o novo número máximo de ações de desfazer para o controle de edição rico. Esse valor pode ser menor que *wParam* se a memória for limitada.

## <a name="remarks"></a>Comentários

Por padrão, o número máximo de ações na fila de desfazer é de 100. Se você aumentar esse número, deverá haver memória suficiente disponível para acomodar o novo número. Para obter um melhor desempenho, defina o limite para o menor valor possível.

Definir o limite como zero desabilita o recurso de **desfazer** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



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

 

 





