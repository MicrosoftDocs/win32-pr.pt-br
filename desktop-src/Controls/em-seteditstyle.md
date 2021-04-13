---
title: Mensagem de EM_SETEDITSTYLE (RichEdit. h)
description: Define os sinalizadores de estilo de edição atuais para um controle de edição rico.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Controles de EM_SETEDITSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499672"
---
# <a name="em_seteditstyle-message"></a>\_Mensagem em SETeditstyle

Define os sinalizadores de estilo de edição atuais para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um ou mais sinalizadores de estilo de edição. Para obter uma lista de valores possíveis, consulte em [**\_ GetEditStyle**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Uma máscara que consiste em um ou mais dos valores *wParam* . Somente os valores especificados nesta máscara serão definidos ou apagados. Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o estado dos sinalizadores de estilo de edição depois que o controle de edição rico tentou implementar as alterações de estilo de edição. Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETeditstyle**](em-geteditstyle.md)
</dt> </dl>

 

 





