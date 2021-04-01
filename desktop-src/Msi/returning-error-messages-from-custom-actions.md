---
description: Esta seção descreve como enviar mensagens de ações personalizadas que realmente executam uma parte da instalação chamando uma biblioteca de vínculo dinâmico ou script.
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: Retornando mensagens de erro de ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480a9e7891680aadc9d8eb4eedba2bad0d2e3dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091131"
---
# <a name="returning-error-messages-from-custom-actions"></a>Retornando mensagens de erro de ações personalizadas

Esta seção descreve como enviar mensagens de ações personalizadas que realmente executam uma parte da instalação chamando uma biblioteca de vínculo dinâmico ou script. Observe que o [tipo de ação personalizada 19](custom-action-type-19.md) envia apenas uma mensagem de erro especificada, retorna falha e, em seguida, encerra a instalação. O tipo de ação personalizada 19 não executa nenhuma parte da instalação.

Para enviar uma mensagem de erro de uma ação personalizada que usa uma dll ( [biblioteca de vínculo dinâmico](dynamic-link-libraries.md) ), faça com que a ação personalizada chame [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). Observe que as ações personalizadas iniciadas por um [ControlEvent, de doação](doaction-controlevent.md) podem enviar mensagens com o método [**Message**](session-message.md) , mas não podem enviar uma mensagem com **MsiProcessMessage**. Em sistemas anteriores ao Windows Server 2003, as ações personalizadas iniciadas por uma ação ControlEvent, não podem enviar mensagens com **MsiProcessMessage** ou método de **mensagem** . Para obter mais informações, consulte [enviando mensagens para Windows Installer usando MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

**Para exibir uma mensagem de erro de dentro de uma ação personalizada usando uma DLL**

1.  A ação personalizada deve chamar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e passar os parâmetros *hInstall*, *eMessageType* e *hRecord*. O identificador para a instalação, [tipo de ação personalizada 19](custom-action-type-19.md), pode ser fornecido para a ação personalizada, conforme descrito em [acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md) ou de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea).
2.  O parâmetro *eMessageType* deve especificar um dos tipos de mensagem, como listado em [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).
3.  O parâmetro *hRecord* da função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende do tipo de mensagem. Consulte [enviando mensagens para Windows Installer usando o MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md). Se a mensagem contiver dados formatados, insira a mensagem na tabela de [erros](error-table.md) usando a formatação descrita em [formatado](formatted.md).

Para enviar uma mensagem de erro de uma ação personalizada que usa [scripts](scripts.md), a ação personalizada pode chamar o método [**Message**](session-message.md) do objeto [**Session**](session-object.md) .

**Para exibir uma mensagem de erro de dentro de uma ação personalizada usando script**

1.  A ação personalizada deve chamar o método [**Message**](session-message.md) do objeto [**Session**](session-object.md) e passar o *tipo* e o *registro* dos parâmetros.
2.  O *tipo* de parâmetro deve especificar um dos tipos de mensagem listados no método [**Message**](session-message.md) .
3.  O parâmetro de *registro* do método [**Message**](session-message.md) depende do tipo de mensagem. Se a mensagem contiver dados formatados, insira a mensagem na tabela de [erros](error-table.md) usando a formatação descrita em [formatado](formatted.md).

As ações personalizadas que usam [arquivos executáveis](executable-files.md) não podem enviar uma mensagem chamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ou o método [**Message**](session-message.md) porque eles não podem obter um identificador para a instalação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Valores de retorno de ação personalizada](custom-action-return-values.md)
</dt> </dl>

 

 



