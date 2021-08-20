---
title: Excluindo uma partição do Diretório do Aplicativo
description: Uma partição de diretório do aplicativo é excluída excluindo o objeto crossRef que representa a partição de diretório do aplicativo.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Excluindo um AD de Partição do Diretório do Aplicativo
- AD de partições do diretório do aplicativo, excluindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3e172fc1633b4d5696e31a8b32cb794721790ea28e93a8d3207f932a789ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019793"
---
# <a name="deleting-an-application-directory-partition"></a>Excluindo uma partição do Diretório do Aplicativo

Uma partição de diretório do aplicativo é excluída excluindo o [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório do aplicativo. Quando a exclusão do objeto **crossRef** for replicada para um controlador de domínio que tenha uma réplica da partição de diretório do aplicativo, o KCC excluirá a réplica local da partição de diretório do aplicativo. Isso eventualmente faz com que todas as réplicas da partição do diretório do aplicativo sejam excluídas.

Quando o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) for excluído, o servidor do Active Directory excluirá o objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) criado quando a partição de diretório do aplicativo foi criada, bem como excluirá todos os objetos na partição de diretório do aplicativo. Nenhum dos objetos na partição do diretório do aplicativo é marcado como exclusão quando eles são excluídos.

Quando uma partição de diretório do aplicativo é excluída, é muito difícil restaurá-la. Para restaurar uma partição de diretório do aplicativo, é necessário restaurar um backup que tenha uma réplica da partição de diretório do aplicativo, encontrar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição do diretório do aplicativo e restaurar o objeto **crossRef** de forma autoritativa.

**Para excluir uma partição de diretório do aplicativo e suas réplicas, execute as etapas a seguir**

1.  Pesquise no contêiner Partições um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome diferenciado da partição de diretório do aplicativo.
2.  [**Exclua o objeto crossRef.**](/windows/desktop/ADSchema/c-crossref)

Para obter mais informações, consulte [Código de exemplo para excluir uma partição do diretório do aplicativo.](example-code-for-deleting-an-application-directory-partition.md)

 

 