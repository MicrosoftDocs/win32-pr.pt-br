---
description: Enviado por uma extensão do Gerenciador de Arquivos para recuperar o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada.
title: FM_GETFOCUS mensagem (Wfext.h)
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
ms.openlocfilehash: e5f6470ea1217485b401387150cae786b44ccca1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841407"
---
# <a name="fm_getfocus-message"></a>Mensagem \_ FM GETFOCUS

Enviado por uma extensão do Gerenciador de Arquivos para recuperar o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tipo de janela do Gerenciador de Arquivos que tem o foco de entrada. Pode ser um dos seguintes valores.



| Código de retorno                                                                                    | Descrição                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**FMFOCUS \_ DIR**</dt> </dl>    | Parte do diretório de uma janela de diretório.<br/> |
| <dl> <dt>**ÁRVORE \_ FMFOCUS**</dt> </dl>   | Parte da árvore de uma janela de diretório.<br/>      |
| <dl> <dt>**UNIDADES \_ FMFOCUS**</dt> </dl> | Barra de unidade de uma janela de diretório.<br/>         |
| <dl> <dt>**PESQUISA DE \_ FMFOCUS**</dt> </dl> | Janela Resultados da Pesquisa.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




