---
description: Os contextos de aplicativo podem ser usados para criar classes lado a lado Windows aplicativo.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Criando classes de Windows lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8317712b333963f9864e195bb1c5f18896dcd73eec059c9c4ae670ff2fb6a4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142339"
---
# <a name="creating-side-by-side-windows-classes"></a>Criando classes de Windows lado a lado

Os contextos de aplicativo podem ser usados para criar classes lado a lado Windows aplicativo. Usando classes lado a lado Windows, seu aplicativo pode ter versões diferentes de uma classe ativa ao mesmo tempo em uma janela pai elegante. Para criar uma classe Windows lado a lado, seu aplicativo deve ativar um contexto de ativação antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obter um alçamento para a nova janela.

Por exemplo, Windows Controles Comuns versão 5.82 e versão 6.0 tinham um controle Editar. Windows padrão é usar o controle Editar versão 5.82. Para obter uma janela lado a lado que tenha o controle Editar versão 6.0, antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costume, seu aplicativo pode referenciar um assembly que expõe classes de janela nomeadas e ativar o contexto de ativação que faz referência aos controles da versão 6.0.

 

 
