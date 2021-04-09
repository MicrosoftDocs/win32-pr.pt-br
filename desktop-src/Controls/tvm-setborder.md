---
title: Mensagem de TVM_SETBORDER (commctrl. h)
description: Define o tamanho da borda para os itens em um controle de exibição de árvore. Você pode enviar a mensagem explicitamente ou usando a \_ macro SetBorder de TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Controles de TVM_SETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824514"
---
# <a name="tvm_setborder-message"></a>\_Mensagem TVM SETborder

**Destinado ao uso interno; Não recomendado para uso em aplicativos.**

Define o tamanho da borda para os itens em um controle de exibição de árvore. Você pode enviar a mensagem explicitamente ou usando a macro [**\_ SetBorder de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizadores de ação. Esse parâmetro pode ser um ou mais dos seguintes valores:



| Valor                                                                                                                                                         | Significado                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Aplica o tamanho de borda especificado ao lado esquerdo dos itens no controle de exibição de árvore. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Aplica o tamanho de borda especificado na parte superior dos itens no controle de exibição de árvore.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **curto** que especifica o tamanho da borda esquerda, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **curto** que especifica o tamanho da borda superior, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **longo** que contém o tamanho da borda anterior, em pixels. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o tamanho anterior da borda horizontal e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o tamanho anterior da borda vertical.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** O uso dessa mensagem pode comprometer a segurança do seu programa.

A borda do item é definida apenas para fins de espaçamento. Uma configuração bem-sucedida dispara um recálculo das barras de rolagem.

Essa mensagem pode não ter suporte em versões futuras do Comctl32.dll. Além disso, essa mensagem não é definida em commctrl. h. Adicione as seguintes definições aos arquivos de origem do seu aplicativo para usar a mensagem:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

