---
title: Mensagem de EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Define o estado atual das opções de tipografia de um controle de edição rico.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Controles de EM_SETTYPOGRAPHYOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918614"
---
# <a name="em_settypographyoptions-message"></a>\_Mensagem em SETtipografiaoptions

Define o estado atual das opções de tipografia de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um ou ambos os valores a seguir.



| Valor                                                                                                                                                                                    | Significado                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**Para \_ ADVANCEDTYPOGRAPHY**</dt> </dl> | A quebra de linha avançada e a formatação de linha estão ativadas. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**PARA \_ SIMPLELINEBREAK**</dt> </dl>             | Quebra de linha mais rápida para texto simples (requer **\_ ADVANCEDTYPOGRAPHY**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma máscara que consiste em um ou mais dos sinalizadores em *wParam*. Somente os sinalizadores definidos nesta máscara serão definidos ou apagados. Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se *wParam* for válido, caso contrário, **false**.

## <a name="remarks"></a>Comentários

A quebra de linha avançada é ativada automaticamente pelo controle de edição rico quando necessário, como para lidar com scripts complexos, como árabe e Hebraico, e para matemática. Eles também são necessários para parágrafos justificados, hifenização e outros recursos tipográficos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETtypographyoptions**](em-gettypographyoptions.md)
</dt> </dl>

 

 





