---
description: O objeto de mesclagem fornece acesso a outros objetos de nível superior. Um objeto de mesclagem deve ser criado antes do carregamento do suporte de automação exigido pelo COM para acessar as funções no Mergemod.dll.
ms.assetid: 3f76ee8a-d195-4a69-99a3-31ef2c1c72d5
title: Mesclar objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1379202d4f252560a381f8af09b30741faa060ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171831"
---
# <a name="merge-object"></a>Mesclar objeto

O objeto de **mesclagem** fornece acesso a outros objetos de nível superior. Um objeto de **mesclagem** deve ser criado antes do carregamento do suporte de automação exigido pelo com para acessar as funções no Mergemod.dll.

Mergemod.dll fornece acesso à funcionalidade estendida no momento da compilação por meio de uma segunda versão do CLSID existente. Esse CLSID dá suporte à funcionalidade existente disponível por meio da interface [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) , mas a interface padrão no objeto (e a interface dupla associada) é a interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) em vez da interface **IMsmMerge** .

 

 
