---
title: Categorizando proxies e stubs DCOM
description: Categorizando proxies e stubs DCOM
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310863"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>Categorizando proxies e stubs DCOM

DCOM realiza o marshaling de referências a objetos por meio da construção de OBJREFs que contêm CLSIDs. Esses CLSIDs são vulneráveis a ataques de segurança porque DLLs arbitrárias podem ser carregadas durante o marshaling. No entanto, o EOAC \_ nenhum \_ sinalizador de \_ marshaling personalizado pode ser especificado ao chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) (consulte [**\_ \_ recursos de autenticação do EOLE**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)). Definir esse sinalizador ajuda a proteger a segurança do servidor ao usar o DCOM, pois reduz as chances de executar DLLs arbitrárias. Quando esse sinalizador é definido, o servidor permite o marshaling somente de CLSIDs que são implementados em ole32.dll, comadmin.dll, comsvcs.dll ou es.dll ou que implementam a \_ ID da categoria do marshaling do CATID.

\_O marshaling do CATID é um GUID de categoria de componente que pode ser associado a um CLSID que está sendo empacotado com marshaling personalizado. As interfaces que são personalizadas empacotadas com esse CLSID são permitidas quando o EOAC \_ nenhum \_ \_ Marshal personalizado é definido por meio de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 