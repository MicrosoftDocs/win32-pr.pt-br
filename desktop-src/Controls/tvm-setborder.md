---
title: TVM_SETBORDER mensagem (Commctrl.h)
description: Define o tamanho da borda para os itens em um controle de exibição de árvore. Você pode enviar a mensagem explicitamente ou usando a macro TreeView \_ SetBorder.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER controles Windows mensagem
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
ms.openlocfilehash: 8d1c8cab133fb654e431638be96301325d68d9743109f84ed8def1ee9cc67c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669651"
---
# <a name="tvm_setborder-message"></a>Mensagem TVM \_ SETBORDER

**Destinado a uso interno; não recomendado para uso em aplicativos.**

Define o tamanho da borda para os itens em um controle de exibição de árvore. Você pode enviar a mensagem explicitamente ou usando a [**macro TreeView \_ SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizadores de ação. Esse parâmetro pode ser um ou mais dos seguintes valores:



| Valor                                                                                                                                                         | Significado                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Aplica o tamanho da borda especificado ao lado esquerdo dos itens no controle de exibição de árvore. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Aplica o tamanho da borda especificado à parte superior dos itens no controle de exibição de árvore.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é **um SHORT** que especifica o tamanho da borda esquerda, em pixels. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é **um SHORT** que especifica o tamanho da borda superior, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor LONG** que contém o tamanho da borda anterior, em pixels. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o tamanho anterior da borda horizontal e [**o HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o tamanho anterior da borda vertical.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem pode comprometer a segurança do programa.

A borda do item é definida apenas para fins de espaçamento. Uma configuração bem-sucedida dispara um recálculo das barras de rolagem.

Essa mensagem pode não ter suporte em versões futuras do Comctl32.dll. Além disso, essa mensagem não está definida em commctrl.h. Adicione as seguintes definições aos arquivos de origem do seu aplicativo para usar a mensagem:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

