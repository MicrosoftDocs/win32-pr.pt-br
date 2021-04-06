---
description: A função AreFileApisANSI determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinando a página de código do conjunto de caracteres atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828602"
---
# <a name="determining-the-current-character-set-code-page"></a>Determinando a página de código do conjunto de caracteres atual

A função [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM. A função [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) faz com que as funções usem a página de código ANSI. A função [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) faz com que as funções usem a página de código OEM.

Por padrão, as funções de e/s de arquivo usam nomes de arquivo ANSI. As funções exportadas por Kernel32.dll que aceitam ou retornam nomes de arquivo são afetadas pela configuração da página de código do arquivo.

[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) e [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) definem a página de código por processo, em vez de por thread ou por computador.

 

 



