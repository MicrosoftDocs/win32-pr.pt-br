---
description: Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando sua barra de ferramentas. Essa mensagem permite que uma DLL de extensão adicione um botão à barra de ferramentas do Gerenciador de arquivos.
title: Mensagem de FMEVENT_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169442"
---
# <a name="fmevent_toolbarload-message"></a>\_Mensagem FMEVENT TOOLBARLOAD

Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando sua barra de ferramentas. Essa mensagem permite que uma DLL de extensão adicione um botão à barra de ferramentas do Gerenciador de arquivos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

O endereço de uma estrutura de [**\_ TOOLBARLOAD do FMS**](fms-toolbarload.md) . Se a extensão DLL adicionar um botão à barra de ferramentas no Gerenciador de arquivos, a DLL deverá preencher a estrutura com informações sobre o botão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma extensão DLL deve retornar **true** para adicionar o botão à barra de ferramentas. Se a DLL retornar **false**, o Gerenciador de arquivos não adicionará o botão.

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

 

 




