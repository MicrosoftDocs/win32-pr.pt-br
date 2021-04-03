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
# <a name="licensing"></a><span data-ttu-id="15b63-103">Licenciamento</span><span class="sxs-lookup"><span data-stu-id="15b63-103">Licensing</span></span>

<span data-ttu-id="15b63-104">Para inserir controles licenciados com êxito, os contêineres de controle ActiveX devem usar [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) em vez de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="15b63-104">In order to embed licensed controls successfully, ActiveX control containers must use [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) instead of [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="15b63-105">Várias funções auxiliares de criação e carregamento de OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) e [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) chamam explicitamente **IClassFactory** e não **IClassFactory2** e, portanto, não podem ser usadas para criar ou carregar controles ActiveX licenciados.</span><span class="sxs-lookup"><span data-stu-id="15b63-105">Several OLE creation and loading helper functions ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) explicitly call **IClassFactory** and not **IClassFactory2**, and therefore cannot be used to create or load licensed ActiveX controls.</span></span> <span data-ttu-id="15b63-106">Os contêineres de controle ActiveX devem criar e carregar explicitamente controles ActiveX usando o **IClassFactory2**.</span><span class="sxs-lookup"><span data-stu-id="15b63-106">ActiveX control containers should explicitly create and load ActiveX Controls using **IClassFactory2**.</span></span>

 

 