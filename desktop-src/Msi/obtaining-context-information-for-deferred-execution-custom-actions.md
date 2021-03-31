---
description: Como o script de instalação pode ser executado fora da sessão de instalação em que foi gravado, a sessão pode não existir mais durante a execução do script de instalação.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Obtendo informações de contexto para ações personalizadas de execução adiada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647653"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Obtendo informações de contexto para ações personalizadas de execução adiada

Como o script de instalação pode ser executado fora da sessão de instalação em que foi gravado, a sessão pode não existir mais durante a execução do script de instalação. Nesse caso, o identificador de sessão original e as propriedades definidas durante a sequência de instalação não estão disponíveis para uma ação personalizada de execução adiada. Todas as funções que exigem um identificador de sessão são restritas a alguns métodos que podem recuperar informações de contexto ou, caso contrário, as propriedades necessárias durante a execução do script devem ser gravadas no script de instalação. Por exemplo, as ações personalizadas adiadas que chamam DLLs (bibliotecas de vínculo dinâmico) passam um identificador que pode ser usado apenas para obter uma quantidade muito limitada de informações. Funções que não exigem um identificador de sessão podem ser acessadas de uma ação personalizada adiada.

As ações personalizadas de execução adiada são restritas à chamada apenas às funções a seguir que exigem um identificador.



| Função                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Dá suporte a um conjunto limitado de propriedades quando usado com [ações personalizadas de execução adiada](deferred-execution-custom-actions.md): a propriedade CustomActionData, a propriedade [**ProductCode**](productcode.md) e a propriedade [**userid**](usersid.md) . As [ações personalizadas de confirmação](commit-custom-actions.md) não podem usar a função [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obter a propriedade [**ProductCode**](productcode.md) . As ações personalizadas de confirmação podem usar a propriedade CustomActionData para obter o código do produto.<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Dá suporte a um conjunto limitado de propriedades quando usado com [ações personalizadas de execução adiada](deferred-execution-custom-actions.md): as propriedades CustomActionData e ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Quando chamado de [ações personalizadas de execução adiada](deferred-execution-custom-actions.md), [confirmação de ações personalizadas](commit-custom-actions.md)ou [reversão de ações personalizadas](rollback-custom-actions.md), [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) retorna true ou false quando solicitado a verificar os parâmetros de modo MSIRUNMODE \_ agendado, MSIRUNMODE \_ Commit ou \_ reversão de MSIRUNMODE. As solicitações para verificar qualquer outro parâmetro do modo de execução de uma ação personalizada adiada, Commit ou Rollback retorna false.<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | A ID do idioma numérico do produto atual. As [ações personalizadas de confirmação](commit-custom-actions.md) não podem usar a função [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) . As ações personalizadas de confirmação podem usar a propriedade CustomActionData para obter a ID do idioma numérico.<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Processa mensagens de erro ou de progresso da ação personalizada.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Uma ação personalizada escrita em JScript ou VBScript requer o objeto de [**sessão**](session-object.md) de instalação. Esse é o objeto de **sessão** de tipo e o instalador o anexa ao script com o nome "Session". Como o objeto de **sessão** pode não existir durante uma reversão de instalação, uma ação personalizada adiada escrita em script deve usar um dos métodos ou propriedades a seguir do objeto de **sessão** para recuperar seu contexto.



| Nome                                                           | Descrição                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade Mode**](session-mode.md)                          | Retorna true para MSIRUNMODE \_ somente agendado.                                                                                       |
| [**Propriedade Property (objeto Session)**](session-session.md)  | Retorna a propriedade CustomActionData, a propriedade [**ProductCode**](productcode.md) ou a propriedade [**userid**](usersid.md) .        |
| [**Propriedade Language (objeto Session)**](session-language.md) | Retorna a ID de idioma numérico da sessão de instalação.                                                                           |
| [**Método de mensagem**](session-message.md)                      | Chamado para tratar erros e progresso.                                                                                              |
| [**Propriedade do instalador**](session-installer.md)                | Retorna o objeto pai, que é usado para funções que não são de sessão, como o acesso do registro e o gerenciamento de configuração do instalador. |



 

Os valores de propriedade que são definidos no momento em que a sequência de instalação é processada no script podem estar indisponíveis no momento da execução do script. Somente o seguinte conjunto limitado de propriedades é sempre acessível para ações personalizadas durante a execução do script.



| Nome da propriedade                      | Descrição                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CustomActionData                   | O valor no momento em que a ação personalizada é processada na tabela de sequência. A propriedade CustomActionData só está disponível para ações personalizadas de execução adiada. As ações personalizadas imediatas não têm acesso a essa propriedade. |
| [**ProductCode**](productcode.md) | Código exclusivo para o produto, uma cadeia de caracteres [GUID](guid.md) .                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Definido pelo instalador para o SID (identificador de segurança) do usuário.                                                                                                                                                   |



 

Se outros dados de propriedade forem exigidos pela ação personalizada de execução adiada, seus valores deverão ser armazenados no script de instalação. Isso pode ser feito usando uma segunda ação personalizada.

**Para gravar o valor de uma propriedade no script de instalação para uso durante uma ação personalizada de execução adiada**

1.  Insira uma pequena ação personalizada na sequência de instalação que define a propriedade de interesse para uma propriedade com o mesmo nome da ação personalizada de execução adiada. Por exemplo, se a chave primária para a ação personalizada de execução adiada for "myaction", defina uma propriedade chamada "myaction" como a propriedade X que você precisa recuperar. Você deve definir a propriedade "myaction" na sequência de instalação antes da ação personalizada "myaction". Embora qualquer tipo de ação personalizada possa definir os dados de contexto, o método mais simples é usar uma ação personalizada de atribuição de propriedade (por exemplo, [tipo de ação personalizada 51](custom-action-type-51.md)).
2.  No momento em que a sequência de instalação é processada, o instalador gravará o valor da propriedade X no script de execução como o valor da propriedade CustomActionData.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> </dl>

 

 




