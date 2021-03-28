---
description: Enviado para um procedimento DLL de extensão do Gerenciador de arquivos quando o Gerenciador de arquivos quiser uma cadeia de caracteres de ajuda para um item de comando de menu ou barra de ferramentas
title: Mensagem de FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169443"
---
# <a name="fmevent_helpstring-message"></a>Mensagem de FMEVENT de \_ ajuda

Enviado para um procedimento DLL de extensão do Gerenciador de arquivos quando o Gerenciador de arquivos quiser uma cadeia de caracteres de ajuda para um item de comando de menu ou barra de ferramentas

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lpfmshs* 
</dt> <dd>

O endereço de uma estrutura de [**\_ HelpString do FMS**](fms-helpstring.md) que comunica dados de cadeia de caracteres de ajuda de item de comando. A **estrutura \_ HelpString do FMS** identifica o item de comando para o qual uma cadeia de caracteres de ajuda é desejada, juntamente com um identificador para seu menu. Em seguida, um aplicativo grava a cadeia de caracteres de ajuda apropriada para o membro **szHelp** da estrutura de **\_ HelpString do FMS** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um procedimento de DLL de extensão deve retornar zero se ele processar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




