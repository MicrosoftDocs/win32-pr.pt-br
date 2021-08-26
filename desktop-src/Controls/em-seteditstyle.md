---
title: EM_SETEDITSTYLE mensagem (Richedit.h)
description: Define os sinalizadores de estilo de edição atuais para um controle de edição rico.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE controles de Windows mensagem
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
ms.openlocfilehash: 06789b1d1fedfc76af205ac46aac7d3ea4bb882f2460676df96cd018d5a216b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048584"
---
# <a name="em_seteditstyle-message"></a>Mensagem \_ EM SETEDITSTYLE

Define os sinalizadores de estilo de edição atuais para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um ou mais sinalizadores de estilo de edição. Para obter uma lista de valores possíveis, [**consulte EM \_ GETEDITSTYLE.**](em-geteditstyle.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Uma máscara que consiste em um ou mais dos *valores wParam.* Somente os valores especificados nesta máscara serão definidos ou limpos. Isso permite que um único sinalizador seja definido ou limpo sem ler os estados do sinalizador atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o estado dos sinalizadores de estilo de edição depois que o controle de edição rich tenta implementar as alterações de estilo de edição. Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





