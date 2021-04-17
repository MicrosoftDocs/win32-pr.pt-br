---
title: Mensagem de SB_SETUNICODEFORMAT (commctrl. h)
description: Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- Controles de SB_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c5223f1e707747356c8869ad047a69f6e8d94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749070"
---
# <a name="sb_setunicodeformat-message"></a>\_Mensagem de SETUNICODEFORMAT SB

Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Determina o conjunto de caracteres que é usado pelo controle. Se esse valor for **true**, o controle usará caracteres Unicode. Se esse valor for **false**, o controle usará caracteres ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o sinalizador de formato Unicode anterior para o controle.

## <a name="remarks"></a>Comentários

Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md)
</dt> </dl>

 

 





