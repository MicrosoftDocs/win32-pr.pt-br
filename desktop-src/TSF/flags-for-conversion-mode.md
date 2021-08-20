---
title: Sinalizadores para o modo de conversão (Ctffunc.h)
description: Os sinalizadores a seguir são usados como um valor de GUID \_ COMPARTMENT \_ KEYBOARD \_ INPUTMODE \_ CONVERSION. Isso é equivalente aos valores CMODE do IME \_ para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Sinalizadores para o modo de conversão Estrutura de Serviços de Texto
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c8c3a452e3115e66e4f0f6e75999cad9bce7e1eadf14b4cadd24fae640a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879212"
---
# <a name="flags-for-conversion-mode"></a>Sinalizadores para o modo de conversão

Os sinalizadores a seguir são usados como um valor de [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ CONVERSION.](predefined-compartments.md) Isso é equivalente aos [valores \_ CMODE do IME](../intl/ime-conversion-mode-values.md) para IMM32.



| Sinalizador                             | Valor  | Descrição                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONVERSIONMODE \_ ALFANUMÉRICO | 0x0000 | Definido como 1 se o modo ALFANUMÉRICO.                                  |
| TF \_ CONVERSIONMODE \_ NATIVE       | 0x0001 | Definido como 1 se o modo NATIVO; 0 se o modo ALFANUMÉRICO.                |
| TF \_ CONVERSIONMODE \_ KATAKANA     | 0x0002 | Definido como 1 se o modo KATAKANA; 0 se o modo HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Definido como 1 se o modo de forma completa; 0 se o modo de forma parcial.              |
| TF \_ CONVERSIONMODE \_ ROMAN        | 0x0010 | Definido como 1 para impedir o processamento de conversões pelo IME; 0 se não. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Definido como 1 se o modo de entrada de código de caractere; 0 se não.                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | Definido como 1 se o modo teclado suave; 0 se não.                       |
| TF \_ CONVERSIONMODE \_ NOCONVERSION | 0x0100 | Definido como 1 para impedir o processamento de conversões pelo IME; 0 se não. |
| SÍMBOLO DE \_ CONVERSÃO DE TFMODE \_       | 0x0400 | Definido como 1 se o modo de conversão SYMBOL; 0 se não.                   |
| TF \_ CONVERSIONMODE \_ FIXO        | 0x0800 | Definido como 1 se o modo de conversão fixo; 0 se não.                    |



 

Os valores a seguir são usados como um valor de [GUID \_ COMPARTMENT KEYBOARD \_ \_ INPUTMODE \_ SENTENCE](predefined-compartments.md). Isso é equivalente aos [valores \_ SMODE do IME](../intl/ime-composition-string-values.md) para IMM32.



| Sinalizador                            | Valor  | Descrição                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ NONE          | 0x0000 | Nenhuma informação para frase.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | O IME usa informações da cláusula plural para realizar o processamento de conversão. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | O IME executa o processamento de conversão no modo de caractere único.        |
| TF \_ SENTENCEMODE \_ AUTOMATIC     | 0x0004 | O IME executa o processamento de conversão no modo automático.               |
| FRASE \_ DE SENTENCEMODE \_ TFPREDICT | 0x0008 | O IME usa informações de frase para prever o próximo caractere.             |
| CONVERSA TF \_ \_ SENTENCEMODE  | 0x0010 | O IME usa o modo de conversa. Isso é útil para aplicativos de chat.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Cabeçalho<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Compartimentos predefinidos](predefined-compartments.md)
</dt> </dl>

 

