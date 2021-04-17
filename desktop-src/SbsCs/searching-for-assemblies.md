---
description: Há dois métodos pelos quais um aplicativo de hospedagem pode pesquisar assemblies lado a lado.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Pesquisando assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747856"
---
# <a name="searching-for-assemblies"></a>Pesquisando assemblies

Há dois métodos pelos quais um aplicativo de hospedagem pode pesquisar assemblies lado a lado.

Os módulos hospedados podem se registrar com o aplicativo de hospedagem, estendendo algumas informações de configuração compartilhadas. O aplicativo pode usar essas informações de configuração para carregar os assemblies necessários para a nova funcionalidade. Isso pode ser feito chamando [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) em manifestos especificados nos dados de registro, seguido chamando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para entrar no novo módulo. Observe que, com esse método, os novos componentes precisam atualizar algum estado do aplicativo compartilhado para indicar sua presença.

O aplicativo de hospedagem pode pesquisar ativamente os assemblies na inicialização usando o [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e o [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para procurar DLLs ou manifestos em um local especificado e, em seguida, usar [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) para acessar as informações. Esse método não requer nenhum registro do componente.

 

 
