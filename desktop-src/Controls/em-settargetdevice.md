---
title: Mensagem de EM_SETTARGETDEVICE (RichEdit. h)
description: Define o dispositivo de destino e a largura da linha usada para \ 0034; o que você vê é o que você obtém \ 0034; (WYSIWYG) em um controle de edição com formatação.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- controles de Windows de mensagem de EM_SETTARGETDEVICE
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697586"
---
# <a name="em_settargetdevice-message"></a>\_Mensagem em SETTARGETDEVICE

Define o dispositivo de destino e a largura da linha usada para a formatação "o que você vê é o que você obtém" (WYSIWYG) em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

HDC para o dispositivo de destino.

</dd> <dt>

*lParam* 
</dt> <dd>

Largura da linha a ser usada para formatação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno será zero se a operação falhar ou for diferente de zero se tiver êxito.

## <a name="remarks"></a>Comentários

O HDC para a impressora padrão pode ser obtido da seguinte maneira.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Se *lParam* for zero, nenhuma quebra de linha será criada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





