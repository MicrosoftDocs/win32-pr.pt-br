---
description: Este exemplo ilustra como criar um pacote de patch que aplica uma pequena atualização ao pacote de instalação de exemplo discutido em Um exemplo de instalação.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Um pequeno exemplo de a patch de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082966"
---
# <a name="a-small-update-patching-example"></a>Um pequeno exemplo de a patch de atualização

Este exemplo ilustra como criar um pacote [](small-updates.md) [de patch](patch-packages.md) que aplica uma pequena atualização ao pacote de instalação de exemplo discutido em Um exemplo [de instalação](an-installation-example.md). Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são considerados muito pequenos para justificar a alteração do código do produto. Para obter mais informações, [consulte Patching and Upgrades](patching-and-upgrades.md).

Este exemplo ilustra como criar um pacote de patch do Windows Installer que atualiza o recurso Concert do produto hipotético MNP2000 para corrigir um erro no produto original. O pacote de patch de exemplo aplica uma pequena atualização ao produto que não requer a alteração do código do produto. Consulte o tópico sobre [Atualizações principais](major-upgrades.md) na seção [Patches e Atualizações](patching-and-upgrades.md) para obter mais informações sobre atualizações principais.

O pacote de atualização de exemplo tem as seguintes especificações:

-   Ele corrige um erro secundário na agenda de shows exibida pelo recurso Concert.
-   Ele atualiza o código do pacote para refletir se o pacote de instalação foi alterado.
-   A pequena atualização pode ser aplicada corrigindo a instalação local do produto.

[Continuar](planning-a-small-update-patch.md)

 

 



