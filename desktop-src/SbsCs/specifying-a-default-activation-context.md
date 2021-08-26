---
description: Especificando um contexto de ativação padrão
ms.assetid: 4d9a8552-7098-458d-a592-45524871cce5
title: Especificando um contexto de ativação padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1598e0a111b358a783b940a5c036d63eef348740ff2467d3ed78720c6a5210
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977136"
---
# <a name="specifying-a-default-activation-context"></a>Especificando um contexto de ativação padrão

Quando seu aplicativo ou componente cria um novo processo, Windows pesquisa um manifesto de aplicativo padrão. Observe que um manifesto incluído como um recurso no aplicativo tem precedência sobre um manifesto externo. O contexto de ativação padrão é o primeiro contexto de ativação que está ativo antes de qualquer outro contexto de ativação ter sido ativado. Esse contexto de ativação está sempre ativo, a menos que você ative outros contextos. Se você definir ISOLATION AWARE ENABLED ao compilar seu aplicativo ou componente, chamadas como \_ \_ [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)e [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) poderão executar o gerenciamento automático de contexto.

O carregador permite que um aplicativo especifique seu contexto de ativação padrão por dois métodos. Você pode colocar o arquivo de manifesto nos recursos do executável e o carregador o encontrará. Isso é o mesmo que colocar o arquivo de manifesto na tabela de recursos do executável. Você pode colocar o manifesto em um arquivo chamado *Myapp*.exe. Manifesto no mesmo diretório que *o Myapp*.exe, e o carregador o localiza enquanto procura *Myapp*.exe.

Se você não usar nenhum desses métodos, o aplicativo começará com o contexto de ativação padrão do sistema, que contém um conjunto mínimo de assemblies.

Uma maneira melhor de usar o gerenciamento automático de contexto é compilando seu aplicativo com ISOLATION \_ AWARE \_ ENABLED definido. O método recomendado é definir isso na linha de comando do compilador para todo o projeto que está sendo compilado em vez de ser definido em arquivos de origem individuais ou em headers. Isso faz com que a maioria das APIs win32 esteja ciente dos contextos de ativação e de como gerenciá-los. Em vez de precisar fazer seu próprio gerenciamento de contexto de ativação, basta colocar um manifesto em sua tabela de recursos na ID do recurso \_ ISOLATIONAWARE MANIFEST RESOURCE ID (valor numérico 2), do tipo \_ \_ RT MANIFEST (valor numérico \_ 24.) Funções como [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)e [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) ativam automaticamente esse contexto antes de fazer a chamada real.

Observe que, se você compilar com ISOLATION AWARE ENABLED definido, também não poderá \_ fazer seu próprio gerenciamento de contexto de \_ ativação. Com ISOLATION AWARE ENABLED definido, Windows ignora qualquer criação de contexto de ativação dinâmica que seu aplicativo possa tentar fazer entre as chamadas \_ \_ [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) e [**CreateWindow.**](/windows/win32/api/winuser/nf-winuser-createwindowa) Isso significa que, quando seu aplicativo usa ISOLATION AWARE ENABLED, você deve garantir que o manifesto contenha uma lista completa de todos os assemblies que \_ \_ seu componente requer.

 

 
