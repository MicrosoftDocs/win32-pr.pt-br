---
description: Subconjunto do .NET 2,0 agora no Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subconjunto do .NET 2,0 agora no Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116144"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Subconjunto do .NET 2,0 agora no Server Core

## <a name="platform"></a>Plataforma

**Servidores** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

A opção de instalação Server Core para o Windows Server 2008 R2 agora inclui um subconjunto do .NET Framework 2,0. O subconjunto é a funcionalidade no .NET 2,0 que se alinha com a funcionalidade no Server Core; nenhum binário foi adicionado à base do Server Core para permitir que qualquer parte do .NET 2,0 funcione.

Não havia suporte ao .NET na opção de instalação do Server Core para o Windows Server 2008.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Isso permite que alguns aplicativos baseados em .NET 2,0 sejam executados no Server Core no Windows Server 2008 R2.

## <a name="testing"></a>Testando

Verifique se as classes .NET usadas pelo seu código estão incluídas no Server Core. Teste também todos os aplicativos que executam esse código no Server Core.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Blog do Server Core](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Consulte também* a seção Server Core do *SDK do Windows Server 2008 R2* quando ele se tornar disponível

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
