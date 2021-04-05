---
title: Sinalizadores para o modo de conversão (Ctffunc. h)
description: Os sinalizadores a seguir são usados como um valor da conversão de teclado do compartimento de GUID de \_ \_ \_ entrada \_ . Isso é equivalente a \_ valores de CMODE do IME para IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Sinalizadores para a estrutura de serviços de texto do modo de conversão
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
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085703"
---
# <a name="flags-for-conversion-mode"></a>Sinalizadores para o modo de conversão

Os sinalizadores a seguir são usados como um valor da [conversão de teclado do compartimento de GUID de \_ \_ \_ entrada \_ ](predefined-compartments.md). Isso é equivalente a valores de [ \_ CMODE do IME](../intl/ime-conversion-mode-values.md) para IMM32.



| Sinalizador                             | Valor  | Descrição                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONversãomode \_ alfanumérico | 0x0000 | Defina como 1 se o modo alfanumérico.                                  |
| TF \_ CONversãomode \_ nativo       | 0x0001 | Defina como 1 se o modo nativo; 0 se o modo alfanumérico.                |
| TF \_ CONversãomode \_ katakana     | 0x0002 | Defina como 1 se modo KATAKANA; 0 se o modo HIRAGANA.                  |
| TF \_ CONversãomode \_ FULLSHAPE    | 0x0008 | Defina como 1 se modo de forma completa; 0 se o modo de meia forma.              |
| TF \_ CONversãomode \_ Roman        | 0x0010 | Defina como 1 para impedir o processamento de conversões por IME; 0 se não for. |
| TF \_ CONversionmode \_ charCode     | 0x0020 | Defina como 1 se o modo de entrada de código de caractere; 0 se não for.                |
| TF \_ CONversãomode \_ SOFTKEYBOARD | 0x0080 | Defina como 1 se o modo de teclado virtual; 0 se não for.                       |
| TF \_ CONversãomode \_ noConversion | 0x0100 | Defina como 1 para impedir o processamento de conversões por IME; 0 se não for. |
| TF \_ símbolo de CONversãomode \_       | 0x0400 | Defina como 1 se modo de conversão de símbolo; 0 se não for.                   |
| TF \_ CONversãomode \_ corrigido        | 0x0800 | Defina como 1 se o modo de conversão fixa; 0 se não for.                    |



 

Os valores a seguir são usados como um valor [de \_ compartimento de GUID \_ teclado \_ InputMode \_ ](predefined-compartments.md). Isso é equivalente a valores de [ \_ SMODE do IME](../intl/ime-composition-string-values.md) para IMM32.



| Sinalizador                            | Valor  | Descrição                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ sentençamode \_ None          | 0x0000 | Nenhuma informação para frase.                                               |
| TF \_ sentençamode \_ PLAURALCLAUSE | 0x0001 | O IME usa as informações de cláusula plural para executar o processamento de conversão. |
| TF \_ sentençamode \_ SINGLECONVERT | 0x0002 | O IME executa o processamento de conversão no modo de caractere único.        |
| TF \_ sentençamode \_ automático     | 0x0004 | O IME executa o processamento de conversão no modo automático.               |
| TF \_ sentençamode \_ PHRASEPREDICT | 0x0008 | O IME usa informações de frase para prever o próximo caractere.             |
| \_conversa TF sentençamode \_  | 0x0010 | O IME usa o modo de conversa. Isso é útil para aplicativos de chat.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 onwindows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| parâmetro<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Compartimentos predefinidos](predefined-compartments.md)
</dt> </dl>

 

