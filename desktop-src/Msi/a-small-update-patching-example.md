---
description: Este exemplo ilustra como criar um pacote de patch que aplica uma pequena atualização ao pacote de instalação de exemplo abordado em um exemplo de instalação.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Um exemplo de aplicação de patch de atualização pequena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750827"
---
# <a name="a-small-update-patching-example"></a>Um exemplo de aplicação de patch de atualização pequena

Este exemplo ilustra como criar um [pacote de patch](patch-packages.md) que aplica uma [pequena atualização](small-updates.md) ao pacote de instalação de exemplo abordado em [um exemplo de instalação](an-installation-example.md). Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são considerados muito pequenos para garantir a alteração do código do produto. Para obter mais informações [, consulte patches e atualizações](patching-and-upgrades.md).

Este exemplo ilustra como criar um pacote de patches Windows Installer que atualiza o recurso de concerto do produto hipotético MNP2000 para corrigir um erro no produto original. O pacote de patch de exemplo aplica uma pequena atualização ao produto que não exige a alteração do código do produto. Consulte o tópico sobre as [principais atualizações](major-upgrades.md) na seção [patches e atualizações](patching-and-upgrades.md) para obter mais informações sobre as principais atualizações.

O pacote de atualização de exemplo tem as seguintes especificações:

-   Ele corrige um erro secundário no cronograma de concerto exibido pelo recurso de concerto.
-   Ele atualiza o código do pacote para refletir que o pacote de instalação foi alterado.
-   A pequena atualização pode ser aplicada por meio da aplicação de patch na instalação local do produto.

[Continuar](planning-a-small-update-patch.md)

 

 



