---
description: Remoção de Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Remoção de Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098516"
---
# <a name="removal-of-windows-movie-maker"></a>Remoção de Windows Movie Maker

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** – Alta  
**Frequência** – Média  


## <a name="description"></a>Descrição

A Microsoft está preterindo e removendo o utilitário Windows Movie Maker aplicativo. Isso inclui:

-   Todos os pontos de entrada Windows Movie Maker (por exemplo, Menu Iniciar, Iniciar > Executar)
-   Todos os binários que foram usados por Windows Movie Maker (tudo o que estava em %ProgramFiles% \\ Movie Maker)

No entanto, os arquivos de projeto Movie Maker usuário permanecerão no sistema e estarão acessíveis a outros aplicativos que deem suporte a esse formato de arquivo.

## <a name="manifestation"></a>Manifestação

Remova os Windows Movie Maker resultados do seguinte:

-   Qualquer tentativa de iniciar o Windows Movie Maker com seus argumentos de linha de comando falhará
-   Todos os plug-ins que foram instalados para habilitar novas transformares e animações permanecerão instalados, mas não serão expostos ao usuário final

## <a name="solution"></a>Solução

Para ter essa funcionalidade no futuro, um usuário precisará instalar um aplicativo semelhante da Microsoft ou de outro provedor de software.

 

 



