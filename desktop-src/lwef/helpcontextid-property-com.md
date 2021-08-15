---
title: Propriedade HelpContextID (objeto Command)
description: Saiba mais sobre a propriedade HelpContextID do objeto Command. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38d0f725c0c809c70fa77b89d3608f8e713fd968c33bfb0192c712f3613e91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478703"
---
# <a name="helpcontextid-property-command-object"></a>Propriedade HelpContextID (objeto Command)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define um número de contexto associado para o [**objeto Command.**](/windows/desktop/lwef/the-command-object) Usado para fornecer Ajuda contextunte para o **objeto Command.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands(""). Número helpContextID_ *  \[  =  \]



| Parte     | Descrição                                   |
|----------|-----------------------------------------------|
| *Número* | Um inteiro que especifica um número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você tiver criado um arquivo de Ajuda Windows para seu aplicativo e tiver definido a propriedade [**HelpFile**](helpfile-property.md) do caractere como o arquivo, o Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário selecionar o comando. Se você definir um número de contexto no [**HelpContextID,**](helpcontextid-property.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o comando.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpFile**](helpfile-property.md)


 

 
