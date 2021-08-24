---
title: Mensagem de EM_SETCARETINDEX (CommCtrl. h)
description: Define o valor de índice baseado em zero da posição do cursor em um controle de edição.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- controles de Windows de mensagem de EM_SETCARETINDEX
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 8b80202ed5294828441abcfa66a914514e31944902e52926de7fa3af92794b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799956"
---
# <a name="em_setcaretindex-message"></a>\_Mensagem em SETCARETINDEX

Define o valor de índice baseado em zero da posição do cursor em um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O novo valor de índice baseado em zero da posição do cursor.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se o índice estiver fora do intervalo do texto em um controle de edição, o índice será ajustado para caber dentro do intervalo do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, 1809 \[ aplicativos de área de trabalho apenas\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2019\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETCARETINDEX**](em-getcaretindex.md)
</dt> </dl>

 

 





