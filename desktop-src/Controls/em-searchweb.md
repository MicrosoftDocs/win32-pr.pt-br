---
title: Mensagem de EM_SEARCHWEB (commctrl. h)
description: Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controles de EM_SEARCHWEB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824643"
---
# <a name="em_searchweb-message"></a>\_Mensagem em SEARCHWEB

Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se o recurso "Pesquisar na Web" for desabilitado usando a mensagem em [**\_ ENABLESEARCHWEB**](em-enablesearchweb.md) , essa mensagem não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





