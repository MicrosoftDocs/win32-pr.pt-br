---
description: 'Para obter um handle para um volume para uso com operações de diário de alteração do USN (número de sequência de atualização), chame a função CreateFile com o parâmetro lpFileName definido como uma cadeia de caracteres do seguinte formato: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Obtendo um alçamento de volume para operações de diário de alteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a7e8090e419df2034d1e1e1726dd74cf2b2915f6976a042a47c73544fa6b38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683476"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Obtendo um alçamento de volume para operações de diário de alteração

Para obter um handle para um volume para uso com operações de diário de alteração do USN (número de sequência de atualização), chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o parâmetro *lpFileName* definido como uma cadeia de caracteres do seguinte formato: \\ \\ . \\ *X:*

Observe que *X* é a letra que identifica a unidade na qual o volume NTFS aparece.

Se o volume não tiver uma letra da unidade, use a sintaxe descrita [em Nomeando um Volume](naming-a-volume.md).

 

 



