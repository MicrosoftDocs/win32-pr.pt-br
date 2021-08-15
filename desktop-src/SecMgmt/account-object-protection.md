---
description: Explica como os objetos de conta são protegidos.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Proteção de objeto de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49610827c8f27b2ad1dd645faca1374534b9d4acb8353421fc55901da724dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969754"
---
# <a name="account-object-protection"></a>Proteção de objeto de conta

[**Os**](account-object.md) objetos de conta são protegidos da seguinte maneira:

-   O grupo **WORLD** tem GENERIC \_ EXECUTE.
-   O grupo **ADMINISTRADOR LOCAL \_** tem acesso DELETE, GENERIC \_ READ, \_ GENERIC WRITE, GENERIC \_ EXECUTE e \_ WRITE DACL.
-   O grupo **ADMINISTRADOR LOCAL \_** é atribuído como proprietário e grupo primário de objetos Account.

 

 



