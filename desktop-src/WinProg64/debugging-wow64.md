---
title: Depurando WOW64
description: Aplicativos em execução no WOW64 podem ser depurados com um depurador hospedado em x86 ou um depurador nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- Programação WOW64 de 64 bits do Windows, depuração
- Depurando programação de WOW64 de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366574"
---
# <a name="debugging-wow64"></a>Depurando WOW64

Os aplicativos em execução no WOW64 podem ser depurados de duas maneiras:

-   Use um depurador hospedado em x86, como o NTSD, o WinDbg ou o Visual Studio. O NTSD de 32 bits é instalado em% SystemRoot% \\ SysWOW64 em instalações de varejo. Observe que os depuradores x86 podem ser usados para depurar código x86, mas não podem ser usados para desmontar ou definir pontos de interrupção dentro da camada de conversão WOW64 porque ele é um código nativo de 64 bits.
-   Use um depurador nativo como o CDB, o NTSD ou o WinDbg e a extensão do depurador WOW64, Wow64exts.dll. Se o depurador nativo for interrompido enquanto o processador estiver no modo x86, o depurador apresentará o processo como um processo x86. Se o processador estiver no modo nativo, o depurador apresentará o processo como nativo.

O CDB, o NTSD e o WinDbg estão incluídos nas ferramentas de depuração para Windows. Para obter mais informações, consulte a documentação sobre [ferramentas de depuração para Windows](/windows-hardware/drivers/debugger/) .

A extensão do depurador do Wow64exts é instalada com o WinDbg. Use o comando! load wow64exts para carregar a extensão do depurador. A tabela a seguir lista os comandos de extensão do depurador! wow64exts.



| Comando                | Descrição                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ! wow64exts. SW          | Alterna entre o modo x86 e nativo.                                                                                                    |
| ! *contagem* de wow64exts. k   | Despeja um rastreamento de pilha de 32 bits/64 bits combinado. Se *Count* for especificado, o comando despejará os primeiros endereços de *contagem* em cada rastreamento de pilha.  |
| ! wow64exts.info        | Despeja informações básicas sobre o PEB do processo, o TEB do thread atual e os slots de armazenamento local de thread (TLS) usados pelo WOW64. |
| ! wow64exts. r *Address* | Despeja o contexto para o endereço especificado. Se o *endereço* não for especificado, o comando despejará o contexto do processador.                     |



 

 

 