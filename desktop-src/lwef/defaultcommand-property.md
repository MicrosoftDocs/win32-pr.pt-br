---
title: Propriedade DefaultCommand
description: Propriedade DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7aec703ffbabb98ae16609b0dcb01767fda5c38b42ed40f204e3a3bae5766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693631"
---
# <a name="defaultcommand-property"></a>Propriedade DefaultCommand

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define o comando padrão do [**objeto Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Caracteres* *  **("**_CharacterID_*_"). Cadeia de caracteres Commands.DefaultCommand_* \[  =  \]



| Parte     | Descrição                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Um valor de cadeia de caracteres que identifica o nome (ID) do [**Comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade permite definir um Comando em [**sua**](/windows/desktop/lwef/the-command-object) coleção [**de Comandos**](/windows/desktop/lwef/the-commands-collection-object) como o comando padrão, renderização em negrito. Na verdade, isso não altera a manipulação de comandos nem os eventos de clique duplo.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

 

 