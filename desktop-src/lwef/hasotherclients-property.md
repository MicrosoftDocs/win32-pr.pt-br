---
title: Propriedade HasOtherClients
description: Propriedade HasOtherClients
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005548"
---
# <a name="hasotherclients-property"></a>Propriedade HasOtherClients

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna se o caractere especificado está sendo usado por outros aplicativos.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente* do. **Caracteres ("***characterid***"). HasOtherClients**



| Valor     | Descrição                                |
|-----------|--------------------------------------------|
| **Verdadeiro**  | O caractere tem outros clientes.           |
| **Falso** | O caractere não tem outros clientes. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode usar essa propriedade para determinar se seu aplicativo é o único ou o último cliente do caractere, quando mais de um aplicativo está compartilhando (carregado) o mesmo caractere.

 

 




