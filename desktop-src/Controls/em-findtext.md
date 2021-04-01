---
title: Mensagem de EM_FINDTEXT (RichEdit. h)
description: Localiza texto em um controle de edição rico.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Controles de EM_FINDTEXT de mensagens do Windows
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
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918625"
---
# <a name="em_findtext-message"></a>\_Mensagem em LocalizarTexto

Localiza texto em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique os parâmetros da operação de pesquisa. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ para baixo**</dt> </dl>                               | Microsoft rich edit 2,0 e posterior: se definido, a pesquisa é do final da seleção atual até o final do documento. Se não estiver definido, a pesquisa será do final da seleção atual até o início do documento. <br/> Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado. A pesquisa é sempre do final da seleção atual até o fim do documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**\_MATCHALEFHAMZA fr**</dt> </dl> | Microsoft Rich Edit 3,0 e posterior: se definido, a pesquisa diferencia entre os Alef árabes com acentos diferentes. Se não estiver definido, todos os Alef serão correspondidos apenas pelo Alef caractere. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará as marcas de diacríticos árabe e Hebraico. Se não estiver definido, as marcas de diacríticos serão ignoradas. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**\_MATCHKASHIDA fr**</dt> </dl>       | Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará kashidas árabes. Se não estiver definido, os kashidas serão ignorados. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**\_MATCHWIDTH fr**</dt> </dl>             | Windows 8: se definido, as versões de byte único e de byte duplo do mesmo caractere são consideradas como não iguais.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**LocalizarTexto**](/windows/win32/api/richedit/ns-richedit-findtexta) que contém informações sobre a operação de localização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência. Se o destino não for encontrado, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

O membro **cpMin** de **LocalizarTexto. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade. Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**. Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





