---
description: Bloco de ambiente de thread (observações de depuração)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloco de ambiente de thread (observações de depuração)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550581"
---
# <a name="thread-environment-block-debugging-notes"></a>Bloco de ambiente de thread (observações de depuração)

O bloco de ambiente de thread ([**estrutura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contém informações de contexto para um thread.

Nas versões a seguir do Windows, o deslocamento do endereço TEB de 32 bits dentro do TEB de 64 bits é 0. Isso pode ser usado para acessar diretamente o TEB de 32 bits de um thread do WOW64. Isso pode ser alterado em versões posteriores do Windows



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

[**Contexto do WOW64 \_**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
