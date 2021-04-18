---
description: 'Para obter um identificador para um volume para uso com operações de diário de alteração de número de sequência de atualização (USN), chame a função CreateFile com o parâmetro lpFileName definido como uma cadeia de caracteres do seguinte formato: \\ \\ . \\ W.x.y..'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtendo um identificador de volume para operações de diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756940"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtendo um identificador de volume para operações de diário de alterações

Para obter um identificador para um volume para uso com operações de diário de alteração de número de sequência de atualização (USN), chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o parâmetro *lpFileName* definido como uma cadeia de caracteres do seguinte formato: \\ \\ . \\ *X*:

Observe que *X* é a letra que identifica a unidade na qual o volume NTFS aparece.

Se o volume não tiver uma letra de unidade, use a sintaxe descrita em [nomeando um volume](naming-a-volume.md).

 

 



