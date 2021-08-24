---
description: Os contextos de ativação permitem que objetos COM sejam usados sem exigir que eles sejam registrados.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Criando Registration-Free objetos COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d5a6c8160eaf15eba4eb799123e0e79d126ccd94b1d4a7a6d332bdb27dd51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142359"
---
# <a name="creating-registration-free-com-objects"></a>Criando Registration-Free objetos COM

Os contextos de ativação permitem que objetos COM sejam usados sem exigir que eles sejam registrados. Isso permite que seu aplicativo tenha vários componentes com funcionalidades diferentes com base em sua versão em vez de suas informações do Registro. Vários componentes podem expor o mesmo objeto COM com o mesmo GUID, mas têm funcionalidades diferentes com base na versão.

Quando um aplicativo solicita um GUID de [**CLSIDFromProgID,**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)o COM primeiro pesquisa o mapeamento de progid para CLSID no contexto de ativação ativa. Quando um aplicativo usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter um ponteiro de interface de instância, o COM pesquisa no contexto de ativação ativa para descobrir qual DLL hospedará o CLSID. Se o contexto de ativação não contém as informações necessárias, o COM pesquisa as informações no Registro usando o método usual.

Observe que, como os contextos de ativação são por thread, o COM faz marshal do contexto de ativação do thread de criação para o thread do host e o ativa antes de chamar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) no thread do host. Essa funcionalidade já está presente no Windows, o código do cliente não precisa fazer nada para implementar isso.

As classes COM podem ser exportadas por componentes hospedados sem passar pelo Registro. Vários componentes podem expor o mesmo ProgID para diferentes objetos COM e seu aplicativo de hospedagem só deve encontrar o contexto de ativação adequado e, em seguida, usar [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obter os ponteiros de interface do objeto hospedado.

 

 
