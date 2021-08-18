---
description: Como obter mais espaço livre em disco depois de exceder a concessão de cota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administração em nível de usuário de cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214f1fb915d199ff6db3a6b3084c5c0f6f2df5c9737290fbdaa0e977a1163f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914356"
---
# <a name="user-level-administration-of-disk-quotas"></a>Administração em nível de usuário de cotas de disco

As cotas de disco são transparentes para o usuário. Quando um usuário solicita a quantidade de espaço livre em um disco, o sistema relata apenas a concessão de cota disponível que o usuário disponibilizou. Se o usuário exceder essa concessão, o sistema retornará o erro de **disco de erro \_ \_ cheio** , assim como seria para indicar que o disco estava cheio.

Para obter mais espaço livre em disco depois de exceder a concessão de cota, o usuário deve seguir um destes procedimentos:

-   Exclua alguns arquivos.
-   Fazer com que outro usuário solicite a propriedade de alguns arquivos.
-   Fazer com que o administrador aumente a concessão de cota.

Os programas que precisam recuperar a quantidade real de espaço livre em disco podem chamar a função [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) e examinar o parâmetro *TotalNumberOfFreeBytes* .

 

 



