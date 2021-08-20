---
title: TB_SETUNICODEFORMAT mensagem (Commctrl.h)
description: TB_SETUNICODEFORMAT mensagem - define o sinalizador de formato de caractere Unicode para o controle . Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de executar, em vez de precisar criar o controle.
ms.assetid: d4eec78d-c25b-4b86-9449-64f091cd8501
keywords:
- TB_SETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9736018fd528f4e59d6fc010e6a1c0c9f95a9f5dbdd056ff5a2eabc96500fb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167429"
---
# <a name="tb_setunicodeformat-message"></a>Mensagem TB \_ SETUNICODEFORMAT

Define o sinalizador de formato de caractere Unicode para o controle . Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de executar, em vez de precisar criar o controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina o conjunto de caracteres usado pelo controle . Se esse valor for diferentes de zero, o controle usará caracteres Unicode. Se esse valor for zero, o controle usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o sinalizador de formato Unicode anterior para o controle .

## <a name="remarks"></a>Comentários

Consulte os comentários de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) uma discussão sobre essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TB \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)
</dt> </dl>

 

 





