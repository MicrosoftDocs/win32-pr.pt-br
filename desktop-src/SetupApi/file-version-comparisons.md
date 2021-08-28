---
description: Se o sinalizador SP COPY NEWER for especificado durante uma operação de cópia de arquivo, as funções de instalação verificarão se há uma cópia existente do arquivo \_ \_ no diretório de destino.
ms.assetid: fd493b5d-7bab-4450-a749-745c536902dc
title: Comparações de versão do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a017549899aa43340f744b1176e7d14ce17d44d60c52b18cfbed9eae3474e99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683176"
---
# <a name="file-version-comparisons"></a>Comparações de versão do arquivo

Se o sinalizador SP COPY NEWER for especificado durante uma operação de cópia de arquivo, as funções de instalação verificarão se há uma cópia existente do arquivo \_ \_ no diretório de destino. Se uma cópia existente for encontrada, as funções compararão as versões do arquivo de destino e de origem para determinar quais são as mais recentes.

As informações de versão do arquivo usadas durante as verificações de versão são especificadas nos membros **dwFileVersionMS** e **dwFileVersionLS** de uma estrutura [**VS \_ FIXEDFILEINFO,**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) usadas pelas funções de versão. Se um dos arquivos não tiver recursos de versão especificados ou se eles têm as mesmas informações de versão, o arquivo de origem será tratado como o arquivo mais recente.

 

 
