---
description: Contextos de ativação permitem que objetos COM sejam usados sem a necessidade de serem registrados.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Criando Registration-Free objetos COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747444"
---
# <a name="creating-registration-free-com-objects"></a>Criando Registration-Free objetos COM

Contextos de ativação permitem que objetos COM sejam usados sem a necessidade de serem registrados. Isso permite que seu aplicativo tenha vários componentes com funcionalidade diferente com base em sua versão, e não nas informações do registro. Vários componentes podem expor o mesmo objeto com com o mesmo GUID, mas têm funcionalidade diferente com base na versão.

Quando um aplicativo solicita um GUID de [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), o com primeiro procura o mapeamento de ProgID para CLSID no contexto de ativação ativa. Quando um aplicativo usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um ponteiro de interface de instância, o com pesquisa o contexto de ativação ativa para descobrir qual DLL hospedará o CLSID. Se o contexto de ativação não contiver as informações necessárias, o COM procurará as informações no registro usando o método usual.

Observe que, como os contextos de ativação são por thread, o COM realiza marshaling do contexto de ativação do thread de criação para o thread de host e o ativa antes de chamar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) no thread do host. Essa funcionalidade já está presente no Windows, o código do cliente não precisa fazer nada para implementar isso.

Classes COM podem ser exportadas por componentes hospedados sem passar pelo registro. Vários componentes podem expor a mesma ProgID para objetos COM diferentes, e seu aplicativo de hospedagem deve localizar apenas o contexto de ativação adequado e, em seguida, usar [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter os ponteiros de interface do objeto hospedado.

 

 
