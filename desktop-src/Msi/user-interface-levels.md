---
description: Windows O instalador fornece aos desenvolvedores de pacotes a capacidade de autor de uma interface do usuário interna que tenha vários níveis de funcionalidade.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Interface do Usuário níveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbe932ea10b62d20ca06a027b935ff04289cdef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478062"
---
# <a name="user-interface-levels"></a>Interface do Usuário níveis

Windows O instalador fornece aos desenvolvedores de pacotes a capacidade de autor de uma interface do usuário interna que tenha vários níveis de funcionalidade. Como a interface do usuário interna deve ser criada pelo autor do pacote, o comportamento da interface do usuário completa, a interface do usuário reduzida, a interface do usuário básica e os níveis Nenhum dependem do pacote de instalação. A tabela a seguir descreve a funcionalidade normalmente atribuída aos níveis de interface do usuário.




| Nível de interface do usuário | Descrição | 
|----------|-------------|
| Interface do usuário completa | Exibe caixas de diálogo modais e sem modo que foram criadas na interface do usuário interna. Exibe caixas de diálogo <a href="error-dialog.md">de erro autoradas.</a><blockquote>[!Note]<br />As caixas de diálogo modais exigem a entrada do usuário antes que a instalação possa continuar e sejam especificadas definindo o Bit de Estilo de Caixa de Diálogo <a href="modal-dialog-style-bit.md">Modal</a> na coluna Atributos da <a href="dialog-table.md">tabela Diálogo.</a> Uma caixa de diálogo sem modo não exige a entrada do usuário para que a instalação continue.</blockquote><br /> Uma interface do usuário completa normalmente exibe o <a href="user-interface-wizard-behavior.md">Interface do Usuário do Assistente.</a><br /> | 
| Interface do usuário reduzida | Exibe todas as caixas de diálogo sem modo que foram autoradas na interface do usuário. Não exibe nenhuma caixa de diálogo modal criada. Exibe caixas de diálogo <a href="error-dialog.md">de erro autoradas.</a> Exibe mensagens <a href="authoring-disk-prompt-messages.md">do Prompt de</a> Disco. Exibe as <a href="filesinuse-dialog.md">caixas de diálogo FilesInUse.</a> | 
| IU básica | Exibe as caixas de diálogo sem modo interno que mostram mensagens de progresso. Exibe caixas de diálogo de erro interno. Não exibe nenhuma caixa de diálogo autorada. Solicita que os usuários insiram um disco exibindo uma caixa de diálogo que contém o valor da propriedade <a href="diskprompt.md"><strong>DiskPrompt.</strong></a> | 
| Nenhum | Nenhum significa uma instalação silenciosa que não exibe nenhuma interface do usuário. | 




 

O nível da interface do usuário interna pode ser definido usando [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). O instalador define a [**propriedade UILevel**](uilevel.md) para o nível atual da interface do usuário.

Se a [**propriedade LIMITUI**](limitui.md) estiver definida, o nível de interface do usuário usado ao instalar o pacote será restrito ao Básico.

Para ver um exemplo de autor da interface do usuário, consulte [Um exemplo de instalação](an-installation-example.md).

 

 




