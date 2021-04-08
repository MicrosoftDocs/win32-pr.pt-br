---
title: Funções de inteiro grandes
description: As funções a seguir são usadas com inteiros grandes.
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aebb5bd8c3edc35098dcf1bb232d858a9c6638d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005661"
---
# <a name="large-integer-functions"></a>Funções de inteiro grandes

As funções a seguir são usadas com inteiros grandes.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                    | Descrição                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | Multiplica dois inteiros de 32 bits assinados, retornando um resultado inteiro assinado de 64 bits.<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | Executa uma operação de deslocamento lógico à esquerda em um valor inteiro de 64 bits sem sinal. A função fornece um código de mudança aprimorado para turnos lógicos à esquerda em que a contagem de deslocamento está no intervalo de 0-31.<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | Executa uma operação de deslocamento aritmético à direita em um valor inteiro de 64 bits assinado. A função fornece um código de mudança aprimorado para deslocamentos aritméticos à direita em que a contagem de deslocamento está no intervalo de 0-31.<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | Executa uma operação de deslocamento lógico à direita em um valor inteiro de 64 bits sem sinal. A função fornece um código de mudança aprimorado para deslocamentos lógicos certos em que a contagem de deslocamento está no intervalo de 0-31.<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | Multiplica os valores de 2 32 bits e divide o resultado de 64 bits por um terceiro valor de 32 bits.<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | Multiplica os inteiros de 2 64 bits para produzir um inteiro de 128 bits.<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | Multiplica os inteiros de 2 64 bits para produzir um inteiro de 128 bits, desloca o produto para a direita pelo número especificado de bits e retorna os baixos 64 bits do resultado.<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | Multiplica os inteiros de 2 64 bits para produzir um inteiro de 128 bits e obtém os altos bits 64.<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | Conta o número de um bits (contagem de população) em um inteiro sem sinal de 64 bits.<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | Turnos de 128 bits à esquerda.<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | Muda para a direita de 128 bits.<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | Multiplica dois inteiros de 32 bits não assinados, retornando um resultado inteiro não assinado de 64 bits.<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | Multiplica dois inteiros de 64 bits sem sinal para produzir um inteiro de 128 bits sem sinal.<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | Multiplica dois inteiros de 64 bits não assinados para produzir um inteiro de 128 bits sem sinal, desloca o produto para a direita pelo número especificado de bits e retorna os baixos 64 bits do resultado.<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | Multiplica os inteiros de 2 64 bits para produzir um inteiro de 128 bits e obtém os bits 64 não assinados altos.<br/>                                                                                                    |



 

 

 





