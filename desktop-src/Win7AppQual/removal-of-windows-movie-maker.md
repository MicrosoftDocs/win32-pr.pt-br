---
description: Remoção do Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Remoção do Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116264"
---
# <a name="removal-of-windows-movie-maker"></a>Remoção do Windows Movie Maker

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -alta  
**Frequência** -média  


## <a name="description"></a>Descrição

A Microsoft está preterindo e removendo o utilitário Windows Movie Maker. Isso inclui:

-   Todos os pontos de entrada para o Windows Movie Maker (por exemplo, menu Iniciar, iniciar > executar)
-   Todos os binários que foram usados pelo Windows Movie Maker (tudo que estava em% ProgramFiles% \\ Movie Maker)

No entanto, os arquivos de projeto do Movie Maker do usuário permanecerão no sistema e poderão ser acessados por outros aplicativos que dão suporte a esse formato de arquivo.

## <a name="manifestation"></a>Manifestação

A remoção do Windows Movie Maker resulta no seguinte:

-   Qualquer tentativa de iniciar o Windows Movie Maker com seus argumentos de linha de comando falhará
-   Os plug-ins que foram instalados para habilitar novas transformações e animações permanecerão instalados, mas não serão expostos ao usuário final

## <a name="solution"></a>Solução

Para ter essa funcionalidade no futuro, um usuário precisará instalar um aplicativo semelhante da Microsoft ou de outro provedor de software.

 

 



