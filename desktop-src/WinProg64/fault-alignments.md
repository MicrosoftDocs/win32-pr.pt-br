---
title: Falhas de alinhamento
description: Falhas de alinhamento
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- falhas de alinhamento 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d813a47cb3428c57ee6235442491f26f8d126a997dd7fcfa6844d551e7958b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412906"
---
# <a name="alignment-faults"></a>Falhas de alinhamento

O manipulador de falha de alinhamento do sistema é desativado por padrão em sistemas baseados em Itanium. Portanto, qualquer acesso a dados não alinhado gera uma exceção que não será automaticamente corrigida pelo sistema, a menos que o aplicativo Capture a exceção em um [manipulador de exceção baseado em quadro](/windows/desktop/Debug/frame-based-exception-handling). Para habilitar o alinhamento do sistema-falha no manipulador, chame a função [**SetError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) com **sem \_ NOALIGNMENTFAULTEXCEPT**. No entanto, observe que os processos podem apresentar uma degradação de desempenho grave se o manipulador de falhas de alinhamento do sistema estiver habilitado e o processo gerar falhas de alinhamento.

Se o depurador do WinDbg tiver sido instalado como o depurador do sistema, o WinDbg será iniciado automaticamente se qualquer processo no sistema gerar uma exceção sem tratamento. Se você não tiver um depurador instalado como o depurador do sistema, o sistema exibirá uma caixa de diálogo informando que seu aplicativo encontrou um erro e fornecendo a oportunidade de relatar o problema à Microsoft.

Em sistemas x64 e ARM64, quaisquer falhas de alinhamento são tratadas por uma combinação de hardware e software. Para obter o melhor desempenho, todo o acesso à memória deve ser corretamente alinhado. Além disso, o [acesso a variáveis interprotegidas](/windows/desktop/Sync/interlocked-variable-access) não alinhadas deve ser evitado em ARM64, pois essas operações não são seguras Atomic.

 

 