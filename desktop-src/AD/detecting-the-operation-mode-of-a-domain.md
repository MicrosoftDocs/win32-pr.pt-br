---
title: Detectando o modo de operação de um domínio
description: No Windows 2000, um domínio pode ser executado em dois modos de operação mistos e nativos.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Detectando o modo de operação de um AD de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823666"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>Detectando o modo de operação de um domínio

No Windows 2000, um domínio pode ser executado em dois modos de operação: misto e nativo. O modo misto deve ser usado para incluir controladores de domínio que executam o Windows NT 4,0 em um domínio do Windows 2000. O modo misto não dá suporte a grupos universais ou grupos aninhados. Se todos os controladores de domínio no domínio estiverem executando o Windows 2000, você poderá usar o modo nativo.

Para detectar programaticamente o modo de operação de um domínio do Windows 2000, leia a propriedade [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) do objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) para esse domínio. Um valor de zero (0) significa que o domínio está no modo nativo. Um valor de um (1) indica que o domínio está no modo misto. Você também pode usar a função [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) para obter o modo de operação, bem como outros dados sobre o domínio e seu estado.

Para associar ao objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) do domínio da conta de usuário sob a qual seu aplicativo está sendo executado, use a associação sem servidor e o RootDSE para obter o nome distinto do domínio e, em seguida, use esse nome distinto para associar ao objeto **domainDns** que representa esse domínio. Para obter mais informações sobre a associação sem servidor e o rootDSE, consulte [associação sem servidor e RootDSE](serverless-binding-and-rootdse.md).

Para obter mais informações e um exemplo de código que mostra como detectar programaticamente o modo de operação de um domínio, consulte [código de exemplo para determinar o modo de operação](example-code-for-determining-the-operation-mode.md).

 

 