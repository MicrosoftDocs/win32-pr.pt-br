---
title: Sequências de chaves
description: Uma cadeia de caracteres de sequência de chaves é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular a tecla press e a sequência de liberação de um teclado padrão no estilo AT de 101 teclas dos EUA.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows PC Virtual de PC Virtual, sequências de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b300c1d417bad30f7a0e06fd8cfb411184eb8f6b800549536c9b6452dcdfefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591441"
---
# <a name="key-sequences"></a>Sequências de chaves

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Uma cadeia de caracteres de sequência de chaves é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular a tecla press e a sequência de liberação de um teclado padrão no estilo AT de 101 teclas dos EUA.

Se um identificador de chave aparecer na cadeia de caracteres sem um modificador anterior, um código pressionado por tecla será simulado, seguido imediatamente pelo código de lançamento de chave correspondente. Os modificadores de chave podem ser usados para alterar esse comportamento.

Por exemplo, o modificador **DOWN** enviará o código pressionado por tecla para o identificador de chave a seguir sem enviar o código liberado por chave. Isso é útil para simular teclas Ctrl, Alt e Shift quando elas são mantidas para baixo enquanto outras chaves estão sendo enviadas. Para liberar a chave, ela deve ser incluída na cadeia de caracteres de chave novamente junto com um modificador **UP** anterior.

## <a name="key-identifiers"></a>Identificadores de chave

A lista a seguir detalha as cadeias de caracteres de identificador de chave válidas. 

| Cadeia de caracteres do identificador de chave | Significado                         |
|-----------------------|---------------------------------|
| Escape de \_ chave           | a **chave Esc**                 |
| Chave \_ F1               | a **tecla F1**                  |
| Chave \_ F2               | a **tecla F2**                  |
| Chave \_ F3               | a **tecla F3**                  |
| Chave \_ F4               | a **tecla F4**                  |
| Chave \_ F5               | a **tecla F5**                  |
| Chave \_ F6               | a **tecla F6**                  |
| Chave \_ F7               | a **tecla F7**                  |
| Chave \_ F8               | a **tecla F8**                  |
| Chave \_ F9               | a **tecla F9**                  |
| Chave \_ F10              | a **tecla F10**                 |
| Chave \_ F11              | a **tecla F11**                 |
| Chave \_ F12              | a **tecla F12**                 |
| Key \_ SysReq           | a **chave SysReq**              |
| Key \_ ScrollLock       | a **tecla ScrollLock**          |
| Quebra de \_ chave            | a **tecla Break**               |
| Key \_ LeftApostrophe   | a **\`** chave                  |
| Chave \_ 1                | a **chave 1**                   |
| Chave \_ 2                | a **tecla 2**                   |
| Chave \_ 3                | a **chave 3**                   |
| Chave \_ 4                | a **chave 4**                   |
| Chave \_ 5                | a **chave 5**                   |
| Chave \_ 6                | a **tecla 6**                   |
| Chave \_ 7                | a **tecla 7**                   |
| Chave \_ 8                | a **tecla 8**                   |
| Chave \_ 9                | a **tecla 9**                   |
| Chave \_ 0                | a **tecla 0**                   |
| \_Hífen de chave           | a **-** chave                   |
| Chave \_ igual a           | a **=** chave                   |
| Backspace \_ de chave        | a **tecla Backspace**           |
| Inserção de \_ chave           | a **tecla Ins**                 |
| Página \_ Principal da Chave             | a **tecla Home**                |
| PageUp \_ de Chave           | a **tecla PageUp**              |
| NumLock \_ de chave          | a **tecla NumLock**             |
| Divisão \_ do KeyPad        | a **/** chave no teclado     |
| Multiplicação \_ do KeyPad      | a **\*** chave no teclado    |
| KeyPad \_ Menos         | a **-** chave no teclado     |
| Guia \_ Chave              | a **tecla Tab**                 |
| Chave \_ Q                | a **tecla Q**                   |
| Chave \_ W                | a **chave W**                   |
| Chave \_ E                | a **chave E**                   |
| Chave \_ R                | a **tecla R**                   |
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
| LeftWindows de chave \_      | a **tecla Left Windows**        |
| Key \_ LeftAlt          | a **tecla Alt esquerda**            |
| Espaço de \_ chave            | a **tecla** Space               |
| Key \_ RightAlt         | a **tecla Alt direita**           |
| Key \_ RightWindows     | a **tecla Windows** direita       |
| Key \_ RightCtrl        | a **tecla Ctrl à** Direita          |
| Aplicativo \_ de chave      | a **chave do** aplicativo         |
| Chave \_ esquerda             | a **tecla Left**                |
| Chave \_ inobada             | a **tecla Down**                |
| Tecla \_ à direita            | a **tecla Right**               |
| KeyPad \_ 0             | a **tecla 0** no teclado     |
| Ponto Decimal do \_ KeyPad  | o **.** chave no teclado     |



 

## <a name="key-modifiers"></a>Modificadores de chave

A lista a seguir detalha as cadeias de caracteres do modificador de chave válidas. 

| Cadeia de caracteres do modificador de chave | Significado                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| PARA BAIXO                | Envie um código pressionado por tecla para o identificador de chave a seguir sem enviar um código liberado por chave. |
| UP                  | Envie um código liberado por chave para o identificador de chave a seguir.                                    |
| HOLD                | Pause 200 milissegundos antes de continuar a processar o restante da cadeia de caracteres de sequência de chaves. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 