---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar o tipo de janela do Gerenciador de arquivos que tem o foco de entrada.
title: Mensagem de FM_GETFOCUS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFOCUS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: e2d5f825-5678-4dd7-adad-eec1cbcc7e49
ms.openlocfilehash: af6e0894b3734f976302eacbf0575a017f054f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967946"
---
# <a name="fm_getfocus-message"></a>Mensagem do FM \_ GETfocus

Enviado por uma extensão do Gerenciador de arquivos para recuperar o tipo de janela do Gerenciador de arquivos que tem o foco de entrada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tipo da janela do Gerenciador de arquivos que tem o foco de entrada. Pode ser um dos seguintes valores.



| Código de retorno                                                                                    | Description                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ dir**</dt> </dl>    | Parte do diretório de uma janela de diretório.<br/> |
| <dl> <dt>**árvore de FMFOCUS \_**</dt> </dl>   | Parte de árvore de uma janela de diretório.<br/>      |
| <dl> <dt>**\_unidades FMFOCUS**</dt> </dl> | Barra de unidades de uma janela de diretório.<br/>         |
| <dl> <dt>**pesquisa do FMFOCUS \_**</dt> </dl> | Janela resultados da pesquisa.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



 

 




