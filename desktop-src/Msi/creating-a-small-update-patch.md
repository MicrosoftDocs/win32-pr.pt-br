---
description: Acate as diretrizes a seguir ao criar um patch para uma pequena atualização Windows Installer.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Criando um pequeno patch de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2c3dffac099358b924914b5dbd86871ba370241c42a2e3fd5caef2d8f12ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379391"
---
# <a name="creating-a-small-update-patch"></a>Criando um pequeno patch de atualização

Ao criar um patch para [pequenas atualizações,](small-updates.md)os autores devem seguir as seguintes diretrizes:

-   Pequenos patches de atualização devem ser projetados para uma única instalação de destino.
-   Pequenos patches de atualização devem usar a versão mais antiga como a instalação de destino.
-   Um pequeno patch de atualização deve substituir e tornar obsoletos os patches de atualização pequenos anteriores.

O cenário a seguir ilustra quando um pequeno patch de atualização é melhor.

Sua empresa envia a versão 1.0 do Myproduct.msi. Logo depois disso, você enviará um pequeno patch [de](small-updates.md) atualização para Myproduct.msi chamado QFE1. Isso não altera a [**propriedade ProductCode**](productcode.md) ou a [**propriedade ProductVersion.**](productversion.md)

Posteriormente, você deve ter um segundo [patch de atualização](small-updates.md) pequeno para Myproduct.msi chamado QFE2. Esse segundo patch deve ser Myproduct.msi versão 1.0. Este segundo patch não deve ser destinado Myproduct.msi versão 1.0 e Myproduct.msi versão 1.0 + QFE1. Quando o QFE2 é aplicado, ele deve remover o QFE1.

 

 



