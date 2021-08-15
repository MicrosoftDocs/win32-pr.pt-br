---
description: Subconjunto do .NET 2.0 Now no Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subconjunto do .NET 2.0 Now no Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9da259186f0eaea7999df6dde6d42d972484c35eee24c9b9efb7fc6a5d882b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994626"
---
# <a name="subset-of-net-20-now-on-server-core"></a>Subconjunto do .NET 2.0 Now no Server Core

## <a name="platform"></a>Plataforma

**Servidores** – Windows Server 2008 R2  



## <a name="feature-impact"></a>Impacto do recurso

 **Gravidade –** Baixa  
**Frequência** – Baixa  





## <a name="description"></a>Descrição

A opção de instalação Server Core Windows Server 2008 R2 agora inclui um subconjunto do .NET Framework 2.0. O subconjunto é a funcionalidade no .NET 2.0 que se alinha à funcionalidade no Server Core; nenhum binário foi adicionado à base Server Core para permitir que qualquer parte do .NET 2.0 funcione.

Não havia suporte para .NET na opção de instalação Server Core para Windows Server 2008.

## <a name="manifestation-of-impact"></a>Manifestação de impacto

Isso permite que alguns aplicativos baseados no .NET 2.0 executem no Server Core no Windows Server 2008 R2.

## <a name="testing"></a>Testando

Verifique se as classes do .NET que seu código usa estão incluídas no Server Core. Teste também todos os aplicativos que executem esse código no Server Core.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Server Core Blog](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   *Consulte também* a seção Server Core do *SDK do Windows Server 2008 R2* quando ele ficar disponível

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
