---
description: Esses escapes são usados com a função ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: Escapes do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff93751450ee6eb6957482362cc8bc22f41d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759392"
---
# <a name="ime-escapes"></a>Escapes do IME

Esses escapes são usados com a função [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea) .



| Escape                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_dicionário de \_ Get \_ EUDC \_ do IME ESC  | Recupere o caminho do arquivo do dicionário EUDC. Na entrada, o parâmetro *lpData* deve ser o ponteiro para o buffer para receber o caminho. Esse buffer deve ser igual ou maior que 80 \* sizeof (TCHAR). No retorno, o buffer contém a cadeia de caracteres terminada em nulo especificando o caminho completo do dicionário. Para uso apenas pelo editor EUDC do chinês; Não use em outros aplicativos.                                                                                  |
| modo de hanja do IME \_ ESC \_ \_            | Converter de Hangul em Hanja. Na entrada, *lpData* deve apontar para o buffer que contém o caractere hangul a ser convertido; na saída, ele recebe o hanja convertido como uma cadeia de caracteres terminada em nulo. Para uso pelo editor coreano; Não use em outros aplicativos.                                                                                                                                                                                                           |
| \_nome do \_ IME \_ ESC do IME              | Recupere o nome do IME. Na entrada, o parâmetro *lpData* deve ser o ponteiro para o buffer para receber o nome. No retorno, o buffer contém a cadeia de caracteres terminada em nulo que especifica o nome do IME. Para uso apenas pelo editor EUDC do chinês; Não use em outros aplicativos. **Windows me/98/95:** O buffer não deve ser inferior a 16 \* sizeof (TCHAR).<br/> **Windows NT, windows 2000, Windows XP:** O buffer não deve ter menos de 64 caracteres.<br/> |
| \_ \_ chave máxima do IME ESC \_               | O valor de retorno da função é o número máximo de Stokes dá de chave para um caractere EUDC. Para uso apenas pelo editor EUDC do chinês; Não use em outros aplicativos.                                                                                                                                                                                                                                                                                                         |
| \_ \_ suporte à consulta do IME ESC \_         | Verifique a implementação. Na entrada, *lpData* aponta para o buffer que contém o valor de escape do IME. A função retornará 0 se o escape não for implementado.                                                                                                                                                                                                                                                                                                             |
| \_sequência ESC do IME \_ \_ para \_ interno | Retorna o código de caractere que corresponde ao código de sequência especificado. Na entrada, o parâmetro *lpData* é o ponteiro para uma variável de 32 bits que contém o código de sequência. Para uso apenas pelo editor EUDC do chinês; Não use em outros aplicativos. Normalmente, o IME do chinês codificará seus códigos de caracteres de leitura na sequência de 1 a n.                                                                                                                               |
| IME \_ ESC \_ set \_ EUDC \_ Dictionary  | Defina o arquivo do dicionário EUDC. Na entrada, o parâmetro *lpData* é o ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho completo. O caminho deve ser inferior a 80 \* sizeof (TCHAR). Para uso apenas pelo editor EUDC do chinês; Não use em outros aplicativos.                                                                                                                                                                                                           |
| IME \_ ESC \_ getarquivodeajudaname        | **Windows me/98, windows 2000, Windows XP:** Retornar o nome do arquivo de ajuda do IME. Em retornar, o parâmetro *lpData* é o caminho completo do arquivo de ajuda do IME. O caminho deve ser inferior a 80 \* sizeof (TCHAR).                                                                                                                                                                                                                                                           |



 

O sistema operacional reserva os escapes no intervalo do IME \_ ESC \_ reservado \_ primeiro para \_ o IME ESC \_ reservado \_ por último para seu próprio uso.

O sistema operacional reserva os escapes no intervalo do IME \_ ESC \_ privado \_ primeiro para o IME \_ ESC \_ privado \_ por último para uso privado por IMEs.

 

 




