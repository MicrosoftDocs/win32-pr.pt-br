---
description: Esta seção descreve a sintaxe e o uso de manipulação de exceção estruturada conforme implementado no compilador de otimização do Microsoft C/C++. As seguintes palavras-chave são interpretadas pelo compilador como parte do mecanismo de manipulação de exceção estruturado.
ms.assetid: 22190b75-417c-49d3-83fe-546018fb61ea
title: Sintaxe do manipulador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c50b8d12a74312c8b0a843ea300d23e278e88
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826170"
---
# <a name="handler-syntax"></a>Sintaxe do manipulador

Esta seção descreve a sintaxe e o uso de manipulação de exceção estruturada conforme implementado no compilador de otimização do Microsoft C/C++. As seguintes palavras-chave são interpretadas pelo compilador como parte do mecanismo de manipulação de exceção estruturado.



| Palavra-chave         | Descrição                                                                                                                                                                                                                                      |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_\_Tente**     | Inicia um corpo de código protegido. Usado com a palavra-chave **\_ \_ Except** para construir um [manipulador de exceção](exception-handler-syntax.md)ou com a palavra-chave **\_ \_ finally** para construir um [manipulador de terminação](termination-handler-syntax.md). |
| **\_\_excepção**  | Inicia um bloco de código que é executado somente quando ocorre uma exceção dentro de seu bloco **\_ \_ try** associado.                                                                                                                                   |
| **\_\_disso** | Inicia um bloco de código que é executado sempre que o fluxo de controle deixa seu bloco **\_ \_ try** associado.                                                                                                                                    |
| **\_\_Deixe**   | Permite o encerramento imediato do bloco **\_ \_ try** sem causar um encerramento anormal e sua penalidade de desempenho.                                                                                                                      |



 

O compilador também interpreta as funções [**GetExceptionCode**](getexceptioncode.md), [**GetExceptionInformation**](getexceptioninformation.md)e [**AbnormalTermination**](abnormaltermination.md) como palavras-chave, e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador. Veja a seguir as breves descrições dessas funções.



| Função                                                   | Descrição                                                                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExceptionCode**](getexceptioncode.md)               | Retorna um código que identifica o tipo de exceção. Essa função pode ser chamada somente de dentro da expressão de filtro ou do bloco de manipulador de exceção.                                                                                                |
| [**GetExceptionInformation**](getexceptioninformation.md) | Retorna um ponteiro para uma [**exceção que \_ aponta**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para uma estrutura contendo ponteiros para o registro de contexto e o registro de exceção. Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção. |
| [**AbnormalTermination**](abnormaltermination.md)         | Indica se o fluxo de controle saiu do bloco **\_ \_ try** associado sequencialmente após a execução da última instrução no bloco. Essa função pode ser chamada somente de dentro do bloco **\_ \_ finally** de um manipulador de encerramento.              |



 

 

 



