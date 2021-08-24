---
title: Licenciamento
description: Licenciamento
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567736"
---
# <a name="licensing"></a>Licenciamento

para inserir controles licenciados com êxito, ActiveX contêineres de controle devem usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) em vez de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). várias funções auxiliares de criação e carregamento de OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chamam explicitamente **IClassFactory** e não **IClassFactory2** e, portanto, não podem ser usadas para criar ou carregar controles de ActiveX licenciados. ActiveX contêineres de controle devem criar e carregar explicitamente ActiveX controles usando **IClassFactory2**.

 

 