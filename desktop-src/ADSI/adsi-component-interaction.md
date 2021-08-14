---
title: Interação do componente ADSI
description: O componente de roteador do Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no Registro quando ele recebe a primeira solicitação do aplicativo cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec82573c23564c964ebe310cd7eceb917a4565ed2d6fa8aa40b4dc03d1db2d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181100"
---
# <a name="adsi-component-interaction"></a>Interação do componente ADSI

O componente de roteador do Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no Registro quando ele recebe a primeira solicitação do aplicativo cliente. Para obter mais informações sobre o Registro, consulte [Instalando o componente provedor de exemplo](installing-the-example-provider-component.md).

As operações que fazem uma solicitação de um diretório para um ponteiro para uma interface em um objeto do Active Directory vêm por meio de uma função (**GetObject** em Visual Basic ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) em C ou C++) ou um método de interface ( [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). Na figura a seguir, o aplicativo cliente ADSI passa essa solicitação de vinculação para o componente de roteador ADSI (1). O componente de roteador identifica o ProgID para o provedor da primeira parte do ADsPath e usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para encontrar o CLSID correspondente no Registro (2) e carrega o componente de provedor adequado (3).

![interações de componente adsi no provedor de exemplo](images/dscspr.png)

Na figura anterior, o componente do provedor cria um objeto do Active Directory que representa o elemento de diretório nomeado. O componente de suporte adsi faz **uma QueryInterface** no identificador de interface solicitado. Quando um ponteiro para essa interface é recuperado (4), assim como acontece com todas as implementações de cliente/servidor COM, ele é passado de volta para o cliente (5) e, a partir daí, o aplicativo cliente funciona diretamente com o componente do provedor (6).

 

 