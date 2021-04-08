---
description: Os contextos de aplicativo podem ser usados para criar classes lado a lado do Windows.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Criando classes lado a lado do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828841"
---
# <a name="creating-side-by-side-windows-classes"></a>Criando classes lado a lado do Windows

Os contextos de aplicativo podem ser usados para criar classes lado a lado do Windows. Usando classes lado a lado do Windows, seu aplicativo pode ter versões diferentes de uma classe ativa ao mesmo tempo em uma janela pai do solitário. Para criar uma classe lado a lado do Windows, seu aplicativo deve ativar um contexto de ativação antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obter um identificador para a nova janela.

Por exemplo, os controles comuns do Windows versão 5,82 e a versão 6,0 tinham um controle de edição. O padrão do Windows é usar o controle de edição da versão 5,82. Para obter uma janela lado a lado que tem o controle de edição da versão 6,0, antes de chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costume, seu aplicativo pode referenciar um assembly que expõe classes de janela nomeadas e, em seguida, ativar o contexto de ativação que faz referência aos controles da versão 6,0.

 

 
