---
title: Propriedade HasOtherClients
description: Propriedade HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479001"
---
# <a name="hasotherclients-property"></a>Propriedade HasOtherClients

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna se o caractere especificado está sendo usado por outros aplicativos.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("**_characterid_*_"). HasOtherClients_*



| Valor     | Descrição                                |
|-----------|--------------------------------------------|
| **Verdadeiro**  | O caractere tem outros clientes.           |
| **Falso** | O caractere não tem outros clientes. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar essa propriedade para determinar se seu aplicativo é o único ou o último cliente do caractere, quando mais de um aplicativo está compartilhando (carregado) o mesmo caractere.

 

 




