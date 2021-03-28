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
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501163"
---
# <a name="fmevent_selchange-message"></a>\_Mensagem FMEVENT SELCHANGE

Enviado a uma DLL de extensão quando o usuário seleciona um nome de arquivo na janela do diretório do Gerenciador de arquivos ou na janela de resultados da pesquisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




