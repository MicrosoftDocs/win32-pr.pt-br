---
title: Mensagem de EM_GETCHARFORMAT (RichEdit. h)
description: Determina a formatação de caractere em um controle de edição rico.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- Controles de EM_GETCHARFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009452"
---
# <a name="em_getcharformat-message"></a>\_Mensagem em GETCHARFORMAT

Determina a formatação de caractere em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o intervalo de texto do qual a formatação deve ser recuperada. Pode ser um dos seguintes valores.



| Valor                                                                                                                                                         | Significado                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**padrão de SCF \_**</dt> </dl>       | A formatação de caractere padrão.<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**seleção de SCF \_**</dt> </dl> | A formatação de caractere da seleção atual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) que recebe os atributos do primeiro caractere. O membro **dwMask** especifica quais atributos são consistentes em toda a seleção. Por exemplo, se toda a seleção estiver em itálico ou não em itálico, o CFM \_ itálico será definido; se a seleção estiver parcialmente em itálico e parcialmente não, o cfm \_ itálico não será definido.

Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , que é uma extensão da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) . Antes de enviar a mensagem em **\_ GETCHARFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o valor do membro **dwMask** da estrutura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





