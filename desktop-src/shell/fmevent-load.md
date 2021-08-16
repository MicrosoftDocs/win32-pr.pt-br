---
description: Enviado para uma DLL de extensão quando o Gerenciador de Arquivos está carregando a DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD mensagem (Wfext.h)
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
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860651"
---
# <a name="fmevent_load-message"></a>Mensagem FMEVENT \_ LOAD

Enviado para uma DLL de extensão quando o Gerenciador de Arquivos está carregando a DLL.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

O endereço de uma estrutura [**FMS \_ LOAD**](fms-load.md) que especifica o valor delta do item de menu.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma DLL de extensão deve retornar **TRUE** para continuar carregando a DLL. Se a DLL retornar **FALSE,** o Gerenciador de Arquivos chamará a [**função FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e terminará qualquer comunicação com a DLL de extensão.

## <a name="remarks"></a>Comentários

Um aplicativo deve preencher os **membros dwSize**, **szMenuName** e **hMenu** na estrutura [**FMS \_ LOAD.**](fms-load.md) Ele também deve salvar o valor do **membro wMenuDelta** e usá-lo para identificar itens de menu ao modificar o menu.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
