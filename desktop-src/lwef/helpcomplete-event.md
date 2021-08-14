---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a41b4dc0b1b6767b113220f2a922d1a512132a2cd7754891acb9c99b92d0039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478991"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Indica que o modo de Ajuda contextitivo foi sair.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *agent.***(ByVal* *  *CharacterID***, ByVal* *  *Name***, ByVal* *  *Cause***)**



| Parte          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retorna a ID do caractere clicado como uma cadeia de caracteres.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nome*        | Retorna um valor de cadeia de caracteres que identifica o nome (ID) do comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Retorna um valor que indica o que causou a conclusão do modo de Ajuda. 1 O usuário selecionou um comando fornecido pelo seu aplicativo.<br/> 2 O usuário selecionou [**o objeto Comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente.<br/> 3 O usuário selecionou o comando Abrir Comandos de Voz.<br/> 4 O usuário selecionou o comando Fechar Comandos de Voz.<br/> 5 O usuário selecionou o comando *Mostrar CharacterName.*<br/> 6 O usuário selecionou o comando *Ocultar CharacterName.*<br/> 7 O usuário selecionou (clicou) o caractere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Normalmente, o modo de Ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere. Clicar em outro caractere ou em outro lugar na tela não cancela o modo de Ajuda. O cliente que definir o modo de Ajuda para o caractere pode cancelar o modo de Ajuda definindo [**HelpModeOn**](helpmodeon-property.md) como **False.** (Isso não dispara o **evento HelpComplete.)**

Quando o usuário seleciona um comando no menu pop-up do caractere no modo ajuda, o servidor remove o menu, chama Ajuda com o [**HelpContextID**](helpcontextid-property.md)especificado do comando e envia esse evento. O contextitivo (também conhecido como O que é isso?) A janela ajuda é exibida no local do ponteiro. Se o usuário selecionar o comando por entrada de voz, a janela Ajuda será exibida sobre o caractere. Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.

Se o servidor retornar Nome como uma cadeia de caracteres vazia (""), isso indicará que o usuário selecionou um comando fornecido pelo servidor.

Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de Ajuda.

### <a name="see-also"></a>Consulte Também

[**Propriedade HelpModeOn**](helpmodeon-property.md), [ **propriedade HelpContextID**](helpcontextid-property.md)


 

