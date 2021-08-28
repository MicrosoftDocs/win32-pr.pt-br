---
description: Bloco de ambiente de thread (notas de depuração)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloco de ambiente de thread (notas de depuração)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f5c40b2a64eb868a7fd3ffb2052a3692db90f19d33357d4ef4f3113803bf52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655266"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloco de ambiente de thread (notas de depuração)

O Bloco de Ambiente de Thread ([**estrutura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contém informações de contexto para um thread.

Nas seguintes versões do Windows, o deslocamento do endereço TEB de 32 bits dentro do TEB de 64 bits é 0. Isso pode ser usado para acessar diretamente o TEB de 32 bits de um thread WOW64. Isso pode mudar em versões posteriores do Windows



|  Plataforma     | Versão                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estruturas de depuração](debugging-structures.md)
</dt> <dt>

[**CONTEXTO \_ WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
