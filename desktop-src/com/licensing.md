---
title: Licenciamento
description: Licenciamento
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641899"
---
# <a name="licensing"></a>Licenciamento

Para inserir controles licenciados com êxito, os contêineres de controle ActiveX devem usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) em vez de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Várias funções auxiliares de criação e carregamento de OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chamam explicitamente **IClassFactory** e não **IClassFactory2** e, portanto, não podem ser usadas para criar ou carregar controles ActiveX licenciados. Os contêineres de controle ActiveX devem criar e carregar explicitamente controles ActiveX usando o **IClassFactory2**.

 

 