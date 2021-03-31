---
title: Excluindo uma partição de diretório de aplicativo
description: Uma partição de diretório de aplicativo é excluída com a exclusão do objeto crossRef que representa a partição de diretório de aplicativo.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Excluindo um AD de partição de diretório de aplicativo
- AD de partições de diretório de aplicativo, excluindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640418"
---
# <a name="deleting-an-application-directory-partition"></a>Excluindo uma partição de diretório de aplicativo

Uma partição de diretório de aplicativo é excluída com a exclusão do objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo. Quando a exclusão do objeto **crossRef** é replicada para um controlador de domínio que tem uma réplica da partição de diretório do aplicativo, o KCC excluirá a réplica local da partição de diretório do aplicativo. Isso eventualmente faz com que todas as réplicas da partição de diretório do aplicativo sejam excluídas.

Quando o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) for excluído, o servidor de Active Directory excluirá o objeto [**domainDns**](/windows/desktop/ADSchema/c-domaindns) que foi criado quando a partição de diretório de aplicativo foi criada, bem como excluirá todos os objetos na partição de diretório de aplicativo. Nenhum dos objetos na partição de diretório de aplicativo é marcado para exclusão quando eles foram excluídos.

Quando uma partição de diretório de aplicativo é excluída, é muito difícil restaurá-la. Para restaurar uma partição de diretório de aplicativo, é necessário restaurar um backup que tenha uma réplica da partição de diretório de aplicativo, localizar o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que representa a partição de diretório de aplicativo e restaurar o objeto **crossRef** com autoridade.

**Para excluir uma partição de diretório de aplicativos e suas réplicas, execute as seguintes etapas**

1.  Pesquise o contêiner partições para obter um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenha um valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) igual ao nome distinto da partição de diretório do aplicativo.
2.  Exclua o objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Para obter mais informações, consulte [código de exemplo para excluir uma partição de diretório de aplicativo](example-code-for-deleting-an-application-directory-partition.md).

 

 