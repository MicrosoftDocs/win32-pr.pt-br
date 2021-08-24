---
title: EM_FINDTEXT mensagem (Richedit.h)
description: EM_FINDTEXT mensagem – localiza o texto dentro de um controle de edição rico.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5fbdff81bfccf63bb0c7804b1aad74e677e77943d6c3d1fa80d19b38c41b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541286"
---
# <a name="em_findtext-message"></a>Mensagem EM \_ FINDTEXT

Localiza o texto em um controle de edição rich.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique os parâmetros da operação de pesquisa. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 e posterior: se definido, a pesquisa será do final da seleção atual ao final do documento. Se não estiver definido, a pesquisa será do final da seleção atual ao início do documento. <br/> Microsoft Rich Edit 1.0: o sinalizador FR \_ DOWN é ignorado. A pesquisa sempre é do final da seleção atual até o final do documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 e posterior: se definido, a pesquisa diferenciará entre as alefs árabe com diferentes acentos. Se não estiver definido, todas as alefs serão corresponder somente pelo caractere alef. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 e posterior: se definido, a operação de pesquisa considerará marcas diacríticas árabe e hebraico. Se não for definido, as marcas diacríticas serão ignoradas. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 e posterior: se definido, a operação de pesquisa considerará kashidas em árabe. Se não estiver definido, kashidas serão ignorados. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: se definidas, as versões de byte único e de byte duplo do mesmo caractere serão consideradas não iguais.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Se definido, a operação pesquisa apenas palavras inteiras que corresponderem à cadeia de caracteres de pesquisa. Se não estiver definida, a operação também procurará fragmentos de palavras que corresponderem à cadeia de caracteres de pesquisa.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que contém informações sobre a operação de local.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da corresponder. Se o destino não for encontrado, o valor de retorno será -1.

## <a name="remarks"></a>Comentários

O **membro cpMin** **de FINDTEXT.chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade. Ao pesquisar para trás, **cpMin** deve ser igual ou maior que **cpMax.** Ao pesquisar para frente, um valor de -1 em **cpMax** estende o intervalo de pesquisa até o final do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Findtext**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





