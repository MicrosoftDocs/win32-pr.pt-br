---
title: Considerações sobre o backup de Active Directory Domain Services
description: Os dados do serviço de diretório podem ser replicados. Um plano de recuperação deve ser criado antes da restauração.
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, planejamento de recuperação
- Active Directory Domain Services Active Directory, backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007350"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Considerações sobre o backup de Active Directory Domain Services

Os dados do serviço de diretório podem ser replicados. Um plano de recuperação deve ser criado antes da restauração. Uma opção é restaurar uma réplica de um diretório e, em seguida, propagar as alterações ocorridas desde o backup de outras réplicas no domínio.

Em alguns casos, talvez você queira que a réplica restaurada tenha precedência sobre as outras réplicas no domínio. Por exemplo, se um objeto for excluído acidentalmente e a exclusão for replicada para todos os controladores de domínio, você poderá restaurar o objeto restaurando uma réplica a partir de um backup que foi feito antes da exclusão do objeto. Em seguida, você usaria o utilitário NTDSUtil para marcar o objeto restaurado como restaurado de forma autoritativa. O objeto restaurado será então replicado para os outros DCs, e a réplica restaurada receberá as atualizações para todos os outros objetos que ocorreram desde a hora em que o backup foi feito. O resultado final de todas as réplicas é o mesmo que antes da restauração, exceto que o objeto restaurado com autoridade não é mais excluído.

Todas as alterações que ocorrem durante o backup são armazenadas em um log temporário e adicionadas ao final do conjunto de backup quando o backup é concluído.

Qualquer plano de recuperação deve garantir que a idade do backup não deve exceder o tempo de vida de Active Directory marca de exclusão. Para obter mais informações sobre o tempo de vida da marca de exclusão, consulte o tópico do TechNet- [introdução à administração de Active Directory backup e recuperação](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)). A restauração de um backup mais antigo que o tempo de vida da marca de exclusão pode fazer com que o controlador de domínio restaurado tenha objetos que não serão replicados em outros DCs. Isso ocorrerá se um objeto for excluído depois que o backup for feito e a restauração ocorrer depois que a marca para exclusão do objeto excluído tiver sido permanentemente removida. O controlador de domínio restaurado teria o objeto como existia antes da exclusão, e os outros DCs não teriam nenhum registro que o objeto já existia. Nesse caso, um administrador precisará excluir manualmente cada objeto não replicado no controlador de domínio restaurado.

Não há suporte para backups incrementais de Active Directory Domain Services; backups completos são necessários.

 

 