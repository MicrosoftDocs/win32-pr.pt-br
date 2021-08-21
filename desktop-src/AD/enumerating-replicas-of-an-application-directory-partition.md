---
title: Enumerando réplicas de uma partição de diretório de aplicativo
description: Este tópico mostra como enumerar as réplicas para uma partição de diretório de aplicativo.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Enumerando réplicas de um AD de partição de diretório de aplicativo
- Partições de diretório de aplicativos AD, enumerando réplicas de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52ff0ea5c2b4737079f4a44997f39dd027299f50c8acd96fe0456b0e5b60d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694883"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Enumerando réplicas de uma partição de diretório de aplicativo

Quando uma réplica de uma partição de diretório de aplicativo é adicionada, o nome distinto do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para o controlador de domínio que conterá a réplica é adicionado ao atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . O objeto **crossRef** usado representa a partição de diretório do aplicativo.

**Para enumerar as réplicas para uma partição de diretório de aplicativo**

1.  Pesquise o contêiner partições para obter um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome distinto da partição de diretório do aplicativo.
2.  Use cada valor do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para associar ao objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) do servidor.
3.  Obtenha o ADsPath para o pai de cada objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) . Esse é um objeto que representa o servidor do controlador de domínio. Use o ADsPath para associar ao objeto de servidor.
4.  Obtenha o valor do atributo [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) do objeto Server. Essa é uma propriedade de valor único que contém o nome DNS do servidor.

Devido à latência de replicação e aos atrasos de execução agendados do KCC, é possível que as réplicas ativas reais para uma partição de diretório de aplicativo não correspondam à lista de controladores de domínio indicados pelo atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Uma maneira mais precisa, mas menos eficiente, de determinar as réplicas ativas reais de uma partição de diretório de aplicativos é Pesquisar todos os objetos [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) na floresta que têm um atributo [**msDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) que contenha o nome distinto da partição de diretório do aplicativo. O atributo **msDS-hasMasterNCs** contém os nomes distintos de todas as partições de diretório graváveis que o controlador de domínio hospeda, incluindo partições de diretório de aplicativo.

 

 