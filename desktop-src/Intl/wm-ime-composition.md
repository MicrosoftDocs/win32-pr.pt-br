---
description: Enviado a um aplicativo quando o IME altera o status da composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Mensagem de WM_IME_COMPOSITION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922905"
---
# <a name="wm_ime_composition-message"></a>Mensagem de composição do \_ IME do WM \_

Enviado a um aplicativo quando o IME altera o status da composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*wParam* 
</dt> <dd>

Caractere DBCS que representa a alteração mais recente na cadeia de caracteres de composição.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que especifica como a cadeia de caracteres de composição ou o caractere foi alterado. Esse parâmetro pode ser um ou mais dos valores a seguir. Para obter mais informações sobre esses valores, consulte [valores da cadeia de caracteres de composição do IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**GCS \_ COMPATTR**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**GCS \_ COMPCLAUSE**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**GCS \_ COMPREADSTR**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**GCS \_ COMPREADATTR**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**GCS \_ COMPREADCLAUSE**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**GCS \_ COMPSTR**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**GCS \_ CURSORPOS**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**GCS \_ DELTASTART**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**GCS \_ RESULTCLAUSE**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**GCS \_ RESULTREADCLAUSE**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**GCS \_ RESULTREADSTR**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**GCS \_ RESULTSTR**
</dt> </dl>

O parâmetro *lParam* também pode ter um ou mais dos valores a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS \_ INSERTCHAR**</dt> </dl>    | Inserir o caractere de composição *wParam* no ponto de inserção atual. Um aplicativo deverá exibir o caractere de composição se ele processar essa mensagem.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ NOMOVECARET**</dt> </dl> | Não mova a posição do cursor como resultado do processamento da mensagem. Por exemplo, se um IME especificar uma combinação de CS \_ INSERTCHAR e cs \_ NOMOVECARET, o aplicativo deverá inserir o caractere especificado na posição atual do cursor, mas não deverá mover o cursor para a próxima posição. Uma mensagem de composição do IME do WM subsequente \_ \_ com GCS \_ RESULTSTR substituirá esse caractere.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deve processar essa mensagem se exibir os próprios caracteres de composição. Caso contrário, ele deve enviar a mensagem para a janela do IME.

Se o aplicativo tiver criado uma janela IME, ele deverá passar essa mensagem para essa janela. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando-a para a janela padrão do IME. A janela IME processa essa mensagem atualizando sua aparência com base no sinalizador de alteração especificado. Um aplicativo pode chamar [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) para recuperar o novo status de composição.

Se nenhum dos valores de GCS \_ for definido, a mensagem indicará que a composição atual foi cancelada e os aplicativos que desenharem a cadeia de caracteres de composição devem excluir a cadeia de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
