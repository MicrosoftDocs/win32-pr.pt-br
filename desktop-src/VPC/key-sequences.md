---
title: Sequências de chave
description: Uma cadeia de caracteres de sequência de chave é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular o pressionamento de tecla e a sequência de versão de um teclado em estilo padrão dos EUA 101.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- PC Virtual PC do Windows, sequências de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c973b5aafd3bf02746ac1550ffedf3d4a4c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641595"
---
# <a name="key-sequences"></a>Sequências de chave

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Uma cadeia de caracteres de sequência de chave é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular o pressionamento de tecla e a sequência de versão de um teclado em estilo padrão dos EUA 101.

Se um identificador de chave aparecer na cadeia de caracteres sem um modificador anterior, um código de chave pressionada será simulado, seguido imediatamente pelo seu código de chave liberada correspondente. Os modificadores de chave podem ser usados para alterar esse comportamento.

Por exemplo, o modificador **down** enviará o código de chave pressionada para o identificador de chave a seguir sem enviar o código de lançamento de chave. Isso é útil para simular as teclas CTRL, ALT e Shift quando elas são mantidas enquanto outras chaves estão sendo enviadas. Para liberar a chave, ela deve ser incluída na cadeia de caracteres de chave novamente junto com um modificador **up** anterior.

## <a name="key-identifiers"></a>Identificadores de chave

A lista a seguir detalha as cadeias de caracteres de identificador de chave válidas. 

| Cadeia de caracteres de identificador de chave | Significado                         |
|-----------------------|---------------------------------|
| Escape de chave \_           | a tecla **ESC**                 |
| Tecla \_ F1               | a tecla **F1**                  |
| Tecla \_ F2               | a tecla **F2**                  |
| Tecla \_ F3               | a tecla **F3**                  |
| Tecla \_ F4               | a tecla **F4**                  |
| Tecla \_ F5               | a tecla **F5**                  |
| Chave \_ F6               | a tecla **F6**                  |
| Tecla \_ F7               | a tecla **F7**                  |
| Tecla \_ F8               | a tecla **F8**                  |
| Tecla \_ F9               | a tecla **F9**                  |
| Tecla \_ F10              | a tecla **F10**                 |
| Tecla \_ F11              | a tecla **F11**                 |
| Tecla \_ F12              | a tecla **F12**                 |
| SysReq de chave \_           | a chave **sysreq**              |
| ScrollLock de chave \_       | a chave **ScrollLock**          |
| Quebra de chave \_            | a chave de **interrupção**               |
| LeftApostrophe de chave \_   | a **\`** chave                  |
| Chave \_ 1                | a chave **1**                   |
| Chave \_ 2                | a chave **2**                   |
| Chave \_ 3                | a tecla **3**                   |
| Chave \_ 4                | a tecla **4**                   |
| Chave \_ 5                | a tecla **5**                   |
| Chave \_ 6                | a chave **6**                   |
| Chave \_ 7                | a tecla **7**                   |
| Chave \_ 8                | a tecla **8**                   |
| Chave \_ 9                | a tecla **9**                   |
| Chave \_ 0                | a chave **0**                   |
| \_Hífen principal           | a **-** chave                   |
| Chave \_ igual a           | a **=** chave                   |
| Backspace da chave \_        | a tecla **Backspace**           |
| Inserção de chave \_           | a chave **ins**                 |
| Início da chave \_             | a chave **inicial**                |
| PageUp de chave \_           | a chave **PageUp**              |
| Tecla \_ NumLock          | a tecla **NumLock**             |
| Divisão do teclado \_        | a **/** chave no teclado     |
| \_Multiplicação do teclado      | a **\*** chave no teclado    |
| Subtração do teclado \_         | a **-** chave no teclado     |
| \_Guia chave              | a tecla **Tab**                 |
| Tecla \_ Q                | a tecla **Q**                   |
| Tecla \_ W                | a tecla **W**                   |
| Chave \_ E                | a chave **E**                   |
| Chave \_ R                | a tecla **R**                   |
| Chave \_ T                | a tecla **T**                   |
| Chave \_ Y                | a chave **Y**                   |
| Chave \_ U                | a tecla **U**                   |
| Chave \_ I                | a tecla **I**                   |
| Chave \_ O                | a **chave o**                   |
| Chave \_ P                | a tecla **P**                   |
| LeftBracket de chave \_      | a **\[** chave                  |
| RightBracket de chave \_     | a **\]** chave                  |
| \_Barra invertida de chave        | a **\\** chave                  |
| Exclusão de chave \_           | a chave de **exclusão**              |
| Fim da chave \_              | a chave **final**                 |
| Chave \_ PageDown         | a chave **PageDown**            |
| Teclado \_ 7             | a tecla **7** no teclado     |
| Teclado \_ 8             | a tecla **8** no teclado     |
| Teclado \_ 9             | a tecla **9** no teclado     |
| Teclado \_ adicional          | a **+** chave no teclado     |
| Chave \_ A                | a **chave a**                   |
| S de chave \_                | a chave **S**                   |
| Chave \_ D                | a tecla **D**                   |
| Chave \_ F                | a tecla **F**                   |
| Chave \_ G                | a tecla **G**                   |
| Tecla \_ H                | a tecla **H**                   |
| Tecla \_ J                | a tecla **J**                   |
| Chave \_ K                | a tecla **K**                   |
| Chave \_ L                | a tecla **L**                   |
| \_Ponto e vírgula chave        | a chave **;**                   |
| SingleQuote de chave \_      | a chave **'**                   |
| Tecla \_ Enter            | a tecla **Enter**               |
| Teclado \_ 4             | a tecla **4** no teclado     |
| Teclado \_ 5             | a tecla **5** no teclado     |
| Teclado \_ 6             | a tecla **6** no teclado     |
| LeftShift de chave \_        | a tecla **SHIFT esquerda**          |
| Chave \_ Z                | a tecla **Z**                   |
| Chave \_ X                | a tecla **X**                   |
| Chave \_ C                | a tecla **C**                   |
| Chave \_ V                | a tecla **V**                   |
| Chave \_ B                | a tecla **B**                   |
| Chave \_ N                | a tecla **N**                   |
| Chave \_ M                | a tecla **M**                   |
| \_Vírgula chave            | a chave **,**                   |
| Período de chave \_           | o **.** chave                   |
| Barra de chave \_            | a **/** chave                   |
| RightShift de chave \_       | a tecla **SHIFT direita**         |
| Chave \_ para cima               | a chave **para cima**                  |
| Teclado \_ 1             | a tecla **1** no teclado     |
| Teclado \_ 2             | a chave **2** no teclado     |
| Teclado \_ 3             | a tecla **3** no teclado     |
| Enter do teclado \_         | a tecla **Enter** no teclado |
| LeftCtrl de chave \_         | a tecla **CTRL esquerda**           |
| LeftWindows de chave \_      | a tecla **Windows esquerda**        |
| LeftAlt de chave \_          | a tecla **ALT esquerda**            |
| Espaço de chave \_            | a chave de **espaço**               |
| RightAlt de chave \_         | a tecla **ALT direita**           |
| RightWindows de chave \_     | a tecla **Windows à direita**       |
| RightCtrl de chave \_        | a tecla **Ctrl direita**          |
| \_Aplicativo principal      | a chave do **aplicativo**         |
| Chave \_ à esquerda             | a tecla **esquerda**                |
| Tecla \_ para baixo             | a tecla **down**                |
| Chave \_ direita            | a chave **direita**               |
| Teclado \_ 0             | a tecla **0** no teclado     |
| DecimalPoint do teclado \_  | o **.** chave no teclado     |



 

## <a name="key-modifiers"></a>Modificadores de chave

A lista a seguir detalha as cadeias de caracteres de modificador de chave válidas. 

| Cadeia de caracteres modificadores de chave | Significado                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| PARA BAIXO                | Envie um código de chave pressionada para o identificador de chave a seguir sem enviar um código de chave lançada. |
| UP                  | Envie um código de chave liberada para o identificador de chave a seguir.                                    |
| HOLD                | Pause 200 milissegundos antes de continuar a processar o restante da cadeia de caracteres da sequência de chaves. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 