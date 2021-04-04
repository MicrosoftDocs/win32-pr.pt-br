---
title: Mensagem de BM_SETIMAGE (WinUser. h)
description: Associa uma nova imagem (ícone ou bitmap) ao botão.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Controles de BM_SETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085290"
---
# <a name="bm_setimage-message"></a>\_Mensagem BM SETimage

Associa uma nova imagem (ícone ou bitmap) ao botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de imagem a ser associado ao botão. Esse parâmetro pode ser um dos seguintes valores:

-   BITMAP de imagem \_
-   ícone de imagem \_

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador (**HICON** ou **HBITMAP**) para a imagem a ser associada ao botão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um identificador para a imagem associada anteriormente ao botão, se houver; caso contrário, será **nulo**.

## <a name="remarks"></a>Comentários

A aparência do texto, um ícone ou ambos em um controle de botão depende do [**\_ ícone de BS**](button-styles.md) e dos estilos de [**\_ bitmap BS**](button-styles.md) , e se a mensagem **\_ SetImage BM** é chamada. Os resultados possíveis são os seguintes:



| \_Ícone de BS ou \_ bitmap BS definido? | BM \_ SetImage chamada? | Resultado              |
|-----------------------------|----------------------|---------------------|
| Sim                         | Sim                  | Mostrar apenas o ícone.     |
| Não                          | Sim                  | Mostrar ícone e texto. |
| Sim                         | Não                   | Mostrar somente texto.     |
| Não                          | Não                   | Mostrar somente texto      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BM \_ GETimage**](bm-getimage.md)
</dt> </dl>

 

 





