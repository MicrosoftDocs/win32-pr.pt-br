---
title: Propriedade HelpContextID (objeto Characters)
description: Saiba mais sobre a propriedade HelpContextID do objeto Characters. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e751cb2d8834a6af2c3b816066d6051e3a28c767
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068178"
---
# <a name="helpcontextid-property-characters-object"></a>Propriedade HelpContextID (objeto Characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define um número de contexto associado para o caractere. Usado para fornecer Ajuda contextul para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Número helpContextID_ *  \[  =  \]



| Parte     | Descrição                                   |
|----------|-----------------------------------------------|
| *Número* | Um inteiro que especifica um número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para dar suporte à Ajuda contextitivo para o caractere, atribua o número de contexto ao caractere que você usa para o tópico de Ajuda associado ao compilar o arquivo de Ajuda. Essa propriedade se aplica somente ao cliente do caractere; a configuração não afeta outros clientes do caractere ou outros caracteres do cliente.

Se você tiver criado um arquivo de Ajuda do Windows para seu aplicativo e definido a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário clicar no caractere. Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o caractere.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Compilador da Ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpFile**](helpfile-property.md)


 

 




