---
description: Uma ação personalizada pode chamar uma função definida em uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: bibliotecas Dynamic-Link (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd2548851dcef4dcf08c53f168ec0f6b43ee036a1c250f9f65f072427a19e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378258"
---
# <a name="dynamic-link-libraries-windows-installer"></a>bibliotecas Dynamic-Link (Windows Instalador)

Uma ação personalizada pode chamar uma função definida em uma DLL (biblioteca de vínculo dinâmico) escrita em C ou C++. A DLL pode existir como um arquivo instalado durante a instalação atual ou como um fluxo binário temporário proveniente da tabela [Binária](binary-table.md) do banco de dados de instalação.

Observe que todas as funções chamadas, incluindo ações personalizadas em DLLs, devem especificar a \_ \_ convenção de chamada stdcall. Por exemplo, para chamar CustomAction, use o seguinte.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Para obter mais informações, [consulte Acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)

Os seguintes tipos de ações personalizadas chamam uma biblioteca de vínculo dinâmico.



| Tipo de ação personalizado                                 | Descrição                               |
|----------------------------------------------------|-------------------------------------------|
| [Tipo de ação personalizada 1](custom-action-type-1.md)   | Arquivo DLL armazenado em um fluxo de tabela binário. |
| [Tipo de ação personalizada 17](custom-action-type-17.md) | Arquivo DLL instalado com um produto.        |



 

> [!Note]  
> Para usar o COM, você precisa chamar [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) na ação personalizada. Não saia se você descobrir que o thread já foi inicializado. Por exemplo, o thread é inicializado em uma instalação por computador, mas não em uma instalação por usuário.

 

Consulte [Lista resumida de todos os](summary-list-of-all-custom-action-types.md) tipos de ação personalizados para ver um resumo de todos os tipos de ações personalizadas e como eles são codificados na tabela [CustomAction](customaction-table.md).

 

 
