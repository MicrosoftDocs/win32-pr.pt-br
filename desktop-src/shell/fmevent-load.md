---
description: Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando a DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Mensagem de FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967939"
---
# <a name="fmevent_load-message"></a>FMEVENT \_ carregar mensagem

Enviado a uma DLL de extensão quando o Gerenciador de arquivos estiver carregando a DLL.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

O endereço de uma estrutura de [**\_ carga do FMS**](fms-load.md) que especifica o valor delta do item de menu.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma extensão DLL deve retornar **true** para continuar carregando a dll. Se a DLL retornar **false**, o Gerenciador de arquivos chamará a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e encerrará qualquer comunicação com a extensão dll.

## <a name="remarks"></a>Comentários

Um aplicativo deve preencher os membros **dwSize**, **szMenuName** e **HMENU** na estrutura de [**\_ carga do FMS**](fms-load.md) . Ele também deve salvar o valor do membro **wMenuDelta** e usá-lo para identificar itens de menu ao modificar o menu.

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

 

 
