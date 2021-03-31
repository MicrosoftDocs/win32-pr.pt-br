---
description: O banco de dados do produto contém informações sobre um produto. Para obter mais informações sobre como obter informações de produto com funções de enumeração, consulte Inicializando um aplicativo.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtendo informações do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921250"
---
# <a name="getting-application-information"></a>Obtendo informações do aplicativo

O banco de dados do produto contém informações sobre um produto. Para obter mais informações sobre como obter informações de produto com funções de enumeração, consulte [inicializando um aplicativo](initializing-an-application.md).

**Para obter informações sobre o produto**

1.  Verifique se um produto está instalado chamando a função [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .
2.  Abra o banco de dados e obtenha um identificador para ele chamando a função [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .

    Se o banco de dados estiver contido em um pacote de instalação, chame a função [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .

3.  Use o identificador aberto para obter propriedades do produto com a função [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) e para obter informações descritivas de recursos com a função [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .

    Se você quiser obter informações de produto usando o código do produto, em vez de usar o identificador de banco de dados aberto, chame a função [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) em vez de [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).

4.  Feche um identificador de instalação aberta chamando a função [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .

    A função [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) é uma função de diagnóstico e não deve ser usada para fechar os identificadores que você sabe que estão abertos. É aceitável chamar a função **MsiCloseAllHandles** quando o aplicativo é fechado para garantir que todos os identificadores tenham sido fechados.

 

 



