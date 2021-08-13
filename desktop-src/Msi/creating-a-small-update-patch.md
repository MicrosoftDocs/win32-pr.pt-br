---
description: siga as diretrizes a seguir ao criar um patch para uma atualização Windows Installer pequena.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Criando um patch de atualização pequena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2c3dffac099358b924914b5dbd86871ba370241c42a2e3fd5caef2d8f12ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379391"
---
# <a name="creating-a-small-update-patch"></a>Criando um patch de atualização pequena

Ao criar um patch para [pequenas atualizações](small-updates.md), os autores devem aderir às seguintes diretrizes:

-   Patches de atualização pequenos devem ser projetados para uma única instalação de destino.
-   Os patches de atualização pequenos devem usar a versão mais antiga como a instalação de destino.
-   Um patch de atualização pequeno deve substituir e tornar obsoleto qualquer patch de atualização pequeno anterior.

O cenário a seguir ilustra quando um patch de atualização pequeno é o melhor.

Sua empresa envia a versão 1,0 do Myproduct.msi. Logo em seguida, você envia um patch de [atualização pequeno](small-updates.md) para Myproduct.msi chamado QFE1. Isso não altera a propriedade [**ProductCode**](productcode.md) ou a propriedade [**ProductVersion**](productversion.md) .

Posteriormente, você cria um segundo patch de [atualização pequena](small-updates.md) para Myproduct.msi chamado QFE2. Esse segundo patch deve ter como destino Myproduct.msi versão 1,0. Esse segundo patch não deve direcionar Myproduct.msi versão 1,0 e Myproduct.msi versão 1,0 + QFE1. Quando QFE2 é aplicado, ele deve remover QFE1.

 

 



