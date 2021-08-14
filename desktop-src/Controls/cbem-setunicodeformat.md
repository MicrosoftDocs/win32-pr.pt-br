---
title: CBEM_SETUNICODEFORMAT mensagem (Commctrl.h)
description: Define o sinalizador de formato de caractere UNICODE para o controle . Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de executar, em vez de precisar criar o controle.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- CBEM_SETUNICODEFORMAT controles de Windows mensagem
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59730922c1d72da90e1c7ba47a287e42ce4ad40375d8216be114e7c280b5a38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699296"
---
# <a name="cbem_setunicodeformat-message"></a>Mensagem CBEM \_ SETUNICODEFORMAT

Define o sinalizador de formato de caractere UNICODE para o controle . Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de executar, em vez de precisar criar o controle.

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

[**CBEM \_ GETUNICODEFORMAT**](cbem-getunicodeformat.md)
</dt> </dl>

 

 





