---
title: Propriedade HelpContextid (objeto characters)
description: Saiba mais sobre a propriedade HelpContextid do objeto Characters. o Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c790f4e3b0e69f4c8dc5e032b0021067e908f4af6200432dae668d08b47e1f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478713"
---
# <a name="helpcontextid-property-characters-object"></a>Propriedade HelpContextid (objeto characters)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define um número de contexto associado para o caractere. Usado para fornecer ajuda contextual para o caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Caracteres Agent. ***("**_characterid_*_")._ *  \[  =  *Número* de HelpContextID\]



| Parte     | Descrição                                   |
|----------|-----------------------------------------------|
| *Número* | Um inteiro que especifica um número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para dar suporte à ajuda contextual para o caractere, atribua o número de contexto ao caractere que você usa para o tópico da ajuda associado ao compilar o arquivo de ajuda. Essa propriedade aplica-se somente ao cliente do caractere; a configuração não afeta outros clientes do caractere ou outros caracteres do cliente.

se você tiver criado um arquivo de ajuda Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) for definido como **True** e o usuário clicar no caractere. Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o caractere.

> [!Note]  
> a criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpFile**](helpfile-property.md)


 

 




