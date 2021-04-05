---
description: Bloco de ambiente de thread (observações de depuração)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloco de ambiente de thread (observações de depuração)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826401"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloco de ambiente de thread (observações de depuração)

O bloco de ambiente de thread ([**estrutura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contém informações de contexto para um thread.

Nas versões a seguir do Windows, o deslocamento do endereço TEB de 32 bits dentro do TEB de 64 bits é 0. Isso pode ser usado para acessar diretamente o TEB de 32 bits de um thread do WOW64. Isso pode ser alterado em versões posteriores do Windows



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas de depuração](debugging-structures.md)
</dt> <dt>

[**Contexto do WOW64 \_**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
