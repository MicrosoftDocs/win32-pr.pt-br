---
description: A figura a seguir ilustra como dois aplicativos podem compartilhar um assembly usando o método tradicional de compartilhamento de assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Compartilhamento de assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922532"
---
# <a name="side-by-side-assembly-sharing"></a>Compartilhamento de assembly lado a lado

A figura a seguir ilustra como dois aplicativos podem compartilhar um assembly usando o método tradicional de compartilhamento de assembly. Um problema com o compartilhamento de assembly tradicional ocorre quando um aplicativo instala uma versão de um assembly, normalmente uma DLL, que não é compatível com versões anteriores. O aplicativo acabou de instalar funciona, mas os aplicativos que dependem da versão anterior da DLL podem não funcionar mais.

![representação de dois aplicativos que compartilham um assembly](images/sxs1.png)

O aplicativo isolado e a solução de assembly lado a lado permitem que versões diferentes do mesmo assembly Win32 sejam executadas ao mesmo tempo no mesmo sistema sem conflito. Ao especificar qual versão do assembly lado a lado o aplicativo deve usar, os desenvolvedores podem garantir que a configuração testada sempre será duplicada no computador do usuário. O compartilhamento lado a lado é ilustrado na figura a seguir.

![implementação de compartilhamento de assembly lado a lado](images/sxs2.png)

Para obter mais informações, consulte [sobre aplicativos isolados e assemblies lado a lado](about-isolated-applications-and-side-by-side-assemblies.md).

 

 



