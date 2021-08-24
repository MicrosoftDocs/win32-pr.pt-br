---
title: Herança de tipo de Pointer-Attribute
description: De acordo com a especificação do DCE, cada arquivo IDL deve definir atributos para seus ponteiros.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf0b365cecf2880fa2746536c3f1d80505f5d7534b95017f8abb18ceecd9d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019256"
---
# <a name="pointer-attribute-type-inheritance"></a>Herança de tipo de Pointer-Attribute

De acordo com a especificação do DCE, cada arquivo IDL deve definir atributos para seus ponteiros. Se um atributo explícito não for atribuído a um ponteiro, o ponteiro usará o valor especificado pela \[ palavra-chave [ \_ default do ponteiro](/windows/desktop/Midl/pointer-default) \] . Algumas implementações de DCE não permitem ponteiros sem atributo. Se um ponteiro não tiver um atributo explícito, o arquivo IDL deverá ter uma especificação de **\[ ponteiro \_ padrão \]** para que o atributo de ponteiro possa ser definido.

No modo padrão (extensões da Microsoft), você pode especificar o atributo de um ponteiro no arquivo IDL que importa o arquivo IDL de definição. Os ponteiros definidos em um arquivo IDL podem herdar atributos que são especificados em outros arquivos IDL. Além disso, no modo padrão, os arquivos IDL podem incluir ponteiros não atributos. Se nem os arquivos IDL base nem importados especificarem um atributo de ponteiro ou **\[ \_ padrão \] de ponteiro**, os ponteiros não atributo serão interpretados como ponteiros exclusivos.

O compilador MIDL atribui atributos de ponteiro a ponteiros usando as seguintes regras de prioridade (1 é a mais alta).



| Prioridade | Descrição                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Atributos de ponteiro explícitos são aplicados ao ponteiro na definição ou no site de uso.                                      |
| 2        | O padrão é o atributo de **\[ ponteiro \_ padrão \]** no arquivo IDL que define o tipo.                               |
| 3        | O padrão é o atributo de **\[ ponteiro \_ padrão \]** no arquivo IDL que importa o tipo.                               |
| 4        | O padrão é \[ [PTR](/windows/desktop/Midl/ptr) \] no modo de compatibilidade com DCE ou \[ [exclusivo](/windows/desktop/Midl/unique) \] no modo de extensões da Microsoft. |



 

 

 