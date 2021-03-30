---
title: Criando uma referência externa
description: Se um objeto crossRef externo for criado e um controlador de domínio o usar para gerar uma referência, o objeto crossRef fornecerá dois elementos de dados importantes nas propriedades a seguir.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- Active Directory de referências externas
- Exemplos de Active Directory Active Directory, criando uma referência externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640422"
---
# <a name="creating-an-external-referral"></a>Criando uma referência externa

Se um objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) externo for criado e um controlador de domínio o usar para gerar uma referência, o objeto **crossRef** fornecerá dois elementos de dados importantes nas propriedades a seguir. Para obter mais informações sobre situações em que isso pode ocorrer, consulte a seção anterior.



| Propriedade                           | Descrição                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Especifica o servidor ou domínio que pode fornecer dados do contexto de nomenclatura especificado no [**NCName**](/windows/desktop/ADSchema/a-ncname).                                           |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Especifica o nome distinto para o domínio, esquema ou contêiner de configuração com raiz no servidor ou domínio especificado por [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot). |



 

Por exemplo, se o servidor com o endereço DNS de serv1.northwest.Fabrikam.com fornece o contexto de nomenclatura com raiz em CN = MyContainer, OU = MyDOM, O = Fabrikam, defina o [**dNSRoot**](/windows/desktop/ADSchema/a-dnsroot) como o endereço DNS desse servidor e o [**NCName**](/windows/desktop/ADSchema/a-ncname) como o nome distinto do contêiner de domínio, esquema ou configuração.

Para obter mais informações e um exemplo de código que mostra como criar uma referência externa, consulte [exemplo de código para criar um objeto crossRef externo](example-code-for-creating-an-external-crossref-object.md).

 

 