---
description: Cada tipo de objeto protegível tem um conjunto de direitos de acesso que correspondem às operações específicas desse tipo de objeto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Direitos de acesso padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56067a4ed31f9506aee0b326e82a9bd5b4b49b02d12e6d401cc04f8262b19da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907106"
---
# <a name="standard-access-rights"></a>Direitos de acesso padrão

Cada tipo de objeto protegível tem um conjunto de direitos de acesso que correspondem às operações específicas desse tipo de objeto. Além desses direitos de acesso específicos ao objeto, há um conjunto de direitos de acesso padrão que correspondem às operações comuns à maioria dos tipos de objetos protegíveis.

O [formato de máscara de acesso](access-mask-format.md) inclui um conjunto de bits para os direitos de acesso padrão. as constantes de Windows a seguir para direitos de acesso padrão são definidas em Winnt. h.



| Constante      | Significado                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE        | O direito de excluir o objeto.                                                                                                                                                                                                                                                                                                              |
| controle de leitura \_ | O direito de ler as informações no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto, sem incluir as informações na SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. |
| SYNCHRONIZE   | O direito de usar o objeto para sincronização. Isso permite que um thread aguarde até que o objeto esteja no estado sinalizado. Alguns tipos de objeto não dão suporte a esse direito de acesso.                                                                                                                                                                |
| GRAVAR \_ DAC    | O direito de modificar a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) no descritor de segurança do objeto.                                                                                                                    |
| proprietário da gravação \_  | O direito de alterar o proprietário no descritor de segurança do objeto.                                                                                                                                                                                                                                                                           |



 

O Winnt. h também define as seguintes combinações de constantes de direitos de acesso padrão.



| Constante                   | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_ \_ todos os direitos padrão      | Combina a exclusão, o \_ controle de leitura, a gravação de \_ DAC, o proprietário da gravação \_ e o acesso de sincronização. |
| \_execução de direitos padrão \_  | Definido atualmente para o controle de leitura igual \_ .                                         |
| \_leitura de direitos padrão \_     | Definido atualmente para o controle de leitura igual \_ .                                         |
| \_direitos padrão \_ necessários | Combina exclusão, \_ controle de leitura, gravação de \_ DAC e \_ acesso de proprietário de gravação.              |
| \_gravação de direitos padrão \_    | Definido atualmente para o controle de leitura igual \_ .                                         |



 

 

 
