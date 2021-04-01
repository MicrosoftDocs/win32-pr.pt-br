---
title: Mensagem de EM_DISPLAYBAND (RichEdit. h)
description: Exibe uma parte do conteúdo de um controle rich edit, conforme formatado anteriormente para um dispositivo usando a mensagem em \_ FormatRange.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- Controles de EM_DISPLAYBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918708"
---
# <a name="em_displayband-message"></a>\_Mensagem em DISPLAYBAND

Exibe uma parte do conteúdo de um controle rich edit, conforme formatado anteriormente para um dispositivo usando a mensagem [**em \_ FORMATRANGE**](em-formatrange.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica a área de exibição do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será **true**.

Se a operação falhar, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Os objetos de texto e Component Object Model (COM) são recortados pelo retângulo. O aplicativo não precisa definir a região de recorte.

A faixa é o processo pelo qual uma única página de saída é gerada usando um ou mais retângulos ou faixas separadas. Quando todas as faixas são colocadas na página, uma imagem completa resulta. Essa abordagem é geralmente usada por impressoras rasterizadas que não têm memória suficiente ou capacidade de fazer a imagem de uma página inteira ao mesmo tempo. Os dispositivos de faixa incluem a maioria das impressoras de matriz de pontos, bem como algumas impressoras a laser.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Imprimindo controles de edição avançada](printing-rich-edit-controls.md)
</dt> </dl>

 

