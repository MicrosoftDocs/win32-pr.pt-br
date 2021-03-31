---
description: As transformações inseridas são armazenadas dentro do arquivo. msi do pacote. Isso garante aos usuários que a transformação está sempre disponível quando o pacote de instalação está disponível. Como alternativa, as transformações podem ser fornecidas aos usuários como arquivos. MST autônomos.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformações inseridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011150"
---
# <a name="embedded-transforms"></a>Transformações inseridas

As transformações inseridas são armazenadas dentro do arquivo. msi do pacote. Isso garante aos usuários que a transformação está sempre disponível quando o pacote de instalação está disponível. Como alternativa, as transformações podem ser fornecidas aos usuários como arquivos. MST autônomos.

Para adicionar uma transformação inserida à lista transformações, adicione dois-pontos (:) prefixo para o nome do arquivo. Como o instalador sempre pode obter a transformação do armazenamento no arquivo. msi, as transformações incorporadas não são armazenadas em cache no computador do usuário. As transformações incorporadas podem ser usadas em combinação com [transformações protegidas](secured-transforms.md) ou [transformações não seguras](unsecured-transforms.md). Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).

 

 



