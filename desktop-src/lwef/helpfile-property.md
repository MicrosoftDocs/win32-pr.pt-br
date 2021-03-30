---
title: Propriedade HelpFile
description: Propriedade HelpFile
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636042"
---
# <a name="helpfile-property"></a>Propriedade HelpFile

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o caminho e o nome do arquivo de uma ajuda sensível ao contexto do Microsoft Windows fornecida pelo aplicativo cliente.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do. ***Caracteres ("*** characterid * * *").* *  \[  =  *Nome de arquivo* do ArquivoDeAjuda\]



| Parte       | Descrição                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Filename* | Uma expressão de cadeia de caracteres especificando o caminho e o nome do arquivo de ajuda do Windows. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade **HelpFile** do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) for definido como **true** e o usuário clicar no caractere ou selecionar um comando no menu pop-up. Se você especificou um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**Propriedade HelpModeOn**](helpmodeon-property.md), [ **propriedade HelpContextID**](helpcontextid-property.md)


 

 




