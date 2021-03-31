---
title: Coleções e grupos
description: A ADSI usa objetos de coleção para representar qualquer conjunto arbitrário de itens em um serviço de diretório que pode ser representado usando o mesmo tipo de dados.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, coleções e grupos
- ADSI de coleções
- ADSI de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917664"
---
# <a name="collections-and-groups"></a>Coleções e grupos

A ADSI usa objetos de coleção para representar qualquer conjunto arbitrário de itens em um serviço de diretório que pode ser representado usando o mesmo tipo de dados. Os objetos de coleção são definidos como um conjunto de valores **variantes** , representando qualquer um dos tipos de dados de automação válidos. Os objetos de coleção podem representar informações persistentes, como listas de controle de acesso e informações voláteis, como trabalhos de impressão em uma fila de impressão.

A Convenção COM padrão para listar o conteúdo de um objeto de coleção (ou contêiner) é criar um objeto enumerador que dê suporte a [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), que tem métodos para percorrer a lista de objetos de coleção. As interfaces na ADSI que fornecem o método **Get \_ \_ NewEnum** (Observe os dois sublinhados) são [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) e [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). A ADSI também fornece às funções auxiliares [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) e [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) para programas C e C++ para simplificar a enumeração. Os clientes de automação usam a enumeração implicitamente quando chamam o **próximo** em um loop **for** .

Os grupos são apenas coleções de objetos que dão suporte à interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .

 

 