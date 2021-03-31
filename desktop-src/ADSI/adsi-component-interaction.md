---
title: Interação do componente ADSI
description: O componente de roteador Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no registro quando ele recebe a primeira solicitação do aplicativo cliente.
ms.assetid: d5438059-1d98-44af-aeac-a3d987990222
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a9ca749e1083ab86335893bef9f4307faee410
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641826"
---
# <a name="adsi-component-interaction"></a>Interação do componente ADSI

O componente de roteador Active Directory popula uma tabela de provedor ADSI dos provedores ADSI instalados listados no registro quando ele recebe a primeira solicitação do aplicativo cliente. Para obter mais informações sobre o registro, consulte [instalando o componente do provedor de exemplo](installing-the-example-provider-component.md).

Operações que fazem uma solicitação de um diretório para um ponteiro para uma interface em um Active Directory objeto passam por uma função (**GetObject** em Visual Basic ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) em C ou C++), ou um método de interface ( [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)). Na figura a seguir, o aplicativo cliente ADSI passa tal solicitação de ligação para o componente de roteador ADSI (1). O componente roteador identifica o ProgID do provedor a partir da primeira parte do ADsPath e usa [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) para localizar o CLSID correspondente no registro (2) e carrega o componente de provedor apropriado (3).

![interações de componente ADSI no provedor de exemplo](images/dscspr.png)

Na figura anterior, o componente do provedor cria um objeto de Active Directory que representa o elemento de diretório nomeado. O componente de suporte ADSI faz um **QueryInterface** no identificador de interface solicitado. Quando um ponteiro para essa interface é recuperado (4), assim como acontece com todas as implementações de cliente/servidor COM, ele é passado de volta para o cliente (5) e, a partir de então, no aplicativo cliente funciona diretamente com o componente do provedor (6).

 

 