---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763818"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Indica que o modo de ajuda contextual foi encerrado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent. * * * (ByVal* *  *characterid * * *, ByVal* *  *Name * * *, ByVal* *  *causa * * *)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nome*        | Retorna um valor de cadeia de caracteres que identifica o nome (ID) do comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Retorna um valor que indica o que causou a conclusão do modo de ajuda. 1 o usuário selecionou um comando fornecido pelo seu aplicativo.<br/> 2 o usuário selecionou o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente.<br/> 3 o usuário selecionou o comando abrir comandos de voz.<br/> 4 o usuário selecionou o comando fechar comandos de voz.<br/> 5 o usuário selecionou o comando Mostrar *caracterename* .<br/> 6 o usuário selecionou o comando Ocultar *caracterename* .<br/> 7 o usuário selecionou (clicou) o caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Normalmente, o modo de ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere. Clicar em outro caractere ou em outro lugar na tela não cancela o modo de ajuda. O cliente que define o modo de ajuda para o caractere pode cancelar o modo de ajuda definindo [**HelpModeOn**](helpmodeon-property.md) como **false**. (Isso não dispara o evento **HelpComplete** .)

Quando o usuário seleciona um comando no menu pop-up do caractere no modo de ajuda, o servidor remove o menu, chama a ajuda com a [**HelpContextId**](helpcontextid-property.md)especificada do comando e envia esse evento. O contexto é contextual (também conhecido como o que é isso?) A janela da ajuda é exibida no local do ponteiro. Se o usuário selecionar o comando por entrada de voz, a janela da ajuda será exibida sobre o caractere. Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.

Se o servidor retornar um nome como uma cadeia de caracteres vazia (""), ele indicará que o usuário selecionou um comando fornecido pelo servidor.

Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de ajuda.

### <a name="see-also"></a>Consulte Também

[**Propriedade HelpModeOn**](helpmodeon-property.md), [ **propriedade HelpContextID**](helpcontextid-property.md)


 

