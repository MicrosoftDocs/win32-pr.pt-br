---
title: Adicionando ou excluindo uma réplica de partição do diretório do aplicativo
description: A primeira réplica de uma partição de diretório de aplicativo é criada no controlador de domínio que foi vinculado a ela no momento da criação.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Adicionando ou excluindo um AD de Réplica de Partição do Diretório do Aplicativo
- AD de partições do diretório do aplicativo, adicionando ou excluindo uma réplica de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adfc63012a6a153d2488e4d3353683ece2d611cb0b3e8e04794eaf76231ab61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024743"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Adicionando ou excluindo uma réplica de partição do diretório do aplicativo

A primeira réplica de uma partição de diretório de aplicativo é criada no controlador de domínio que foi vinculado a ela no momento da criação. Réplicas adicionais podem ser criadas em qualquer controlador de domínio na floresta, não necessariamente no mesmo domínio que o controlador de domínio inicial. Uma réplica de partição do diretório do aplicativo só pode existir em um controlador de domínio que está executando Windows Server 2003 ou posterior. Para obter mais informações, consulte este artigo do TechNet sobre Gerenciamento [de Partições](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Para adicionar uma réplica para uma partição de diretório de aplicativo, execute as etapas a seguir**

1.  Pesquise no contêiner Partições um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome diferenciado da partição de diretório do aplicativo.
2.  A bind ao [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) com a delegação habilitada. Isso é necessário porque o **objeto crossRef** só pode ser modificado no Domain-Naming de função FSMO. Com a delegação habilitada, o controlador de domínio pode entrar em contato com o Domain-Naming de função FSMO usando as mesmas credenciais.
3.  Adicione o nome diferenciado do objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para o controlador de domínio que hospedará a nova réplica ao atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do [**objeto crossRef.**](/windows/desktop/ADSchema/c-crossref)

Quando o novo valor do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) for replicado para o novo controlador de domínio que hospedará uma réplica da partição de diretório do aplicativo, o KCC será disparado para replicar a partição de diretório do aplicativo para o controlador de domínio de destino.

Para remover uma réplica de uma partição de diretório de aplicativo, execute as mesmas etapas acima para localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório do aplicativo e remover o valor que corresponde ao controlador de domínio do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) do **objeto crossRef.**

Quando o novo valor do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) for replicado para o controlador de domínio que não hospedará mais uma réplica da partição de diretório do aplicativo, o KCC será disparado para remover a réplica da partição de diretório do aplicativo no controlador de domínio de destino.

Se um controlador de domínio que está hospedando uma réplica de partição de diretório do aplicativo for removido ou rebaixado, o servidor do Active Directory removerá automaticamente o valor correspondente ao controlador de domínio do atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de todos os [**objetos crossRef.**](/windows/desktop/ADSchema/c-crossref)

 

 