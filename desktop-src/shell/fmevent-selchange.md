---
description: Enviado a uma DLL de extensão quando o usuário seleciona um nome de arquivo na janela do diretório do Gerenciador de arquivos ou na janela de resultados da pesquisa.
title: Mensagem de FMEVENT_SELCHANGE (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: befc217eeb24453d7db726cf68d233fa57e5a7971fd148406cf90810b52b070d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459033"
---
# <a name="fmevent_selchange-message"></a>\_Mensagem FMEVENT SELCHANGE

Enviado a uma DLL de extensão quando o usuário seleciona um nome de arquivo na janela do diretório do Gerenciador de arquivos ou na janela de resultados da pesquisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma DLL de extensão deve retornar zero se ela processar essa mensagem.

## <a name="remarks"></a>Comentários

As alterações na parte da árvore da janela do diretório não produzem essa mensagem.

Como o usuário pode alterar a seleção várias vezes, a DLL de extensão deve retornar imediatamente após o processamento dessa mensagem para evitar a lentidão do processo de seleção para o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




