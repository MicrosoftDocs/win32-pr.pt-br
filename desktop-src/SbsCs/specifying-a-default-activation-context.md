---
description: Especificando um contexto de ativação padrão
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Especificando um contexto de ativação padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32cf0225a8e4290a09f7e6524a4b3ef47f9c4c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922531"
---
# <a name="specifying-a-default-activation-context"></a>Especificando um contexto de ativação padrão

Quando seu aplicativo ou componente cria um novo processo, o Windows procura um manifesto de aplicativo padrão. Observe que um manifesto incluído como um recurso no aplicativo tem precedência sobre um manifesto externo. O contexto de ativação padrão é o primeiro contexto de ativação que está ativo antes de qualquer outro contexto de ativação ter sido ativado. Esse contexto de ativação sempre estará ativo, a menos que você ative outros contextos. Se você definir \_ o reconhecimento \_ de isolamento habilitado quando compilar seu aplicativo ou componente, chamadas como [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) podem executar o gerenciamento automático de contexto.

O carregador permite que um aplicativo especifique seu contexto de ativação padrão por dois métodos. Você pode colocar o arquivo de manifesto nos recursos do executável e o carregador irá encontrá-lo. Isso é o mesmo que colocar o arquivo de manifesto na tabela de recursos do executável. Você pode inserir o manifesto em um arquivo chamado *MyApp*. exe. O manifesto no mesmo diretório que o *MyApp*. exe e o carregador o encontra enquanto procura *MyApp*. exe.

Se você usar nenhum desses métodos, o aplicativo começará com o contexto de ativação padrão do sistema, que contém um conjunto mínimo de assemblies.

Uma maneira melhor de usar o gerenciamento automático de contexto é compilar seu aplicativo com \_ reconhecimento \_ habilitado para isolamento definido. O método recomendado é definir isso na linha de comando do compilador para todo o projeto que está sendo compilado, em vez de ser definido em arquivos ou cabeçalhos de origem individuais. Isso faz com que a maioria das APIs do Win32 reconheça os contextos de ativação e como gerenciá-los. Em vez de precisar fazer seu próprio gerenciamento de contexto de ativação, basta colocar um manifesto em sua tabela de recursos na ID do recurso \_ ISOLATIONAWARE \_ \_ ID do recurso de manifesto (valor numérico 2), do manifesto do tipo RT \_ (valor numérico 24.) Funções como [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ativam automaticamente esse contexto antes de fazer a chamada real.

Observe que, se você compilar com \_ reconhecimento de isolamento \_ habilitado definido, também não poderá fazer seu próprio gerenciamento de contexto de ativação. Com o \_ reconhecimento de isolamento \_ habilitado definido, o Windows ignora qualquer criação de contexto de ativação dinâmica que seu aplicativo pode tentar fazer entre chamadas [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . Isso significa que, quando seu aplicativo usa o \_ reconhecimento \_ de isolamento habilitado, você deve certificar-se de que o manifesto contém uma lista completa de todos os assemblies que seu componente requer.

 

 
