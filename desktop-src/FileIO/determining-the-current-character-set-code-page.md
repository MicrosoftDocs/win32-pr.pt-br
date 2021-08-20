---
description: A função AreFileApisANSI determina se as funções de E/S de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinando a página de código do conjunto de caracteres atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150653"
---
# <a name="determining-the-current-character-set-code-page"></a>Determinando a página de código do conjunto de caracteres atual

A [**função AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se as funções de E/S de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM. A [**função SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) faz com que as funções usem a página de código ANSI. A [**função SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) faz com que as funções usem a página de código OEM.

Por padrão, as funções de E/S de arquivo usam nomes de arquivo ANSI. As funções exportadas por Kernel32.dll que aceitam ou retornam nomes de arquivo são afetadas pela configuração da página de código de arquivo.

[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) e [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) configuram a página de código por processo, em vez de por thread ou por computador.

 

 



