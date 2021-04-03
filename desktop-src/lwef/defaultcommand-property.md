---
title: Propriedade DefaultCommand
description: Propriedade DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007473"
---
# <a name="defaultcommand-property"></a>Propriedade DefaultCommand

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o comando padrão do objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent. * * * caracteres* *  **("***Characterid***"). Commands. DefaultCommand** \[  =  *String*\]



| Parte     | Descrição                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Um valor de cadeia de caracteres que identifica o nome (ID) do [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade permite que você defina um [**comando**](/windows/desktop/lwef/the-command-object) em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) como o comando padrão, renderizando-o em negrito. Isso não altera de fato o tratamento de comandos nem eventos de clique duplo.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

 

 