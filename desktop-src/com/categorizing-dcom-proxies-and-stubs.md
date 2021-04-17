---
title: Categorizando proxies e stubs DCOM
description: Categorizando proxies e stubs DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31685cd1318856b9e305246cfebc2cebb3a7874e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105782563"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a><span data-ttu-id="db31b-103">Categorizando proxies e stubs DCOM</span><span class="sxs-lookup"><span data-stu-id="db31b-103">Categorizing DCOM Proxies and Stubs</span></span>

<span data-ttu-id="db31b-104">DCOM realiza o marshaling de referências a objetos por meio da construção de OBJREFs que contêm CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="db31b-104">DCOM marshals references to objects by constructing OBJREFs that contain CLSIDs.</span></span> <span data-ttu-id="db31b-105">Esses CLSIDs são vulneráveis a ataques de segurança porque DLLs arbitrárias podem ser carregadas durante o marshaling.</span><span class="sxs-lookup"><span data-stu-id="db31b-105">These CLSIDs are vulnerable to security attacks because arbitrary DLLs can be loaded during marshaling.</span></span> <span data-ttu-id="db31b-106">No entanto, o EOAC \_ nenhum \_ sinalizador de \_ marshaling personalizado pode ser especificado ao chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consulte [**\_ \_ recursos de autenticação do EOLE**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span><span class="sxs-lookup"><span data-stu-id="db31b-106">However, the EOAC\_NO\_CUSTOM\_MARSHAL flag can be specified when calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (see [**EOLE\_AUTHENTICATION\_CAPABILITIES**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)).</span></span> <span data-ttu-id="db31b-107">Definir esse sinalizador ajuda a proteger a segurança do servidor ao usar o DCOM, pois reduz as chances de executar DLLs arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="db31b-107">Setting this flag helps protect server security when using DCOM because it reduces the chances of executing arbitrary DLLs.</span></span> <span data-ttu-id="db31b-108">Quando esse sinalizador é definido, o servidor permite o marshaling somente de CLSIDs que são implementados em ole32.dll, comadmin.dll, comsvcs.dll ou es.dll ou que implementam a \_ ID da categoria do marshaling do CATID.</span><span class="sxs-lookup"><span data-stu-id="db31b-108">When this flag is set, the server allows the marshaling only of CLSIDs that are implemented in ole32.dll, comadmin.dll, comsvcs.dll, or es.dll, or that implement the CATID\_MARSHALER category ID.</span></span>

<span data-ttu-id="db31b-109">\_O marshaling do CATID é um GUID de categoria de componente que pode ser associado a um CLSID que está sendo empacotado com marshaling personalizado.</span><span class="sxs-lookup"><span data-stu-id="db31b-109">CATID\_MARSHALER is a component category GUID that can be associated with a CLSID that is being custom marshaled.</span></span> <span data-ttu-id="db31b-110">As interfaces que são personalizadas empacotadas com esse CLSID são permitidas quando o EOAC \_ nenhum \_ \_ Marshal personalizado é definido por meio de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="db31b-110">The interfaces being custom marshaled with this CLSID are allowed when the EOAC\_NO\_CUSTOM\_MARSHAL is set via [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db31b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db31b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db31b-112">Categorias de componentes</span><span class="sxs-lookup"><span data-stu-id="db31b-112">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 