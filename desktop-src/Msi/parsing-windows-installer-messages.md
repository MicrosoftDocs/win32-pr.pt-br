---
description: Um manipulador de interface do usuário externo pode processar a lista de mensagens do instalador especificado pelo parâmetro dwMessagedFilter da função MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analisando mensagens de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165237"
---
# <a name="parsing-windows-installer-messages"></a>Analisando mensagens de Windows Installer

Um manipulador de interface do usuário externo pode processar a lista de mensagens do instalador especificado pelo parâmetro *dwMessagedFilter* da função [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . Algumas dessas mensagens contêm cadeias de caracteres que podem ser usadas diretamente, e outras mensagens podem precisar ser analisadas e processadas pelo manipulador de interface do usuário externo para serem úteis. O manipulador de interface do usuário externa pode precisar apenas monitorar Windows Installer mensagens sem executar nenhuma operação que afete a instalação.

As mensagens de Windows Installer a seguir contêm cadeias de caracteres que podem ser exibidas por uma caixa de diálogo e não precisam de processamento adicional. Essas mensagens contêm uma lista de botões e ícones que devem ser exibidos por uma caixa de diálogo. Você pode usar os valores de **MB \_ ICONMASK**, **MB \_ DEFMASK** e **MB \_ TYPEMASK** para especificar ícones e botões.

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**
</dt> <dd>

Ocorreu um encerramento prematuro da instalação.

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**erro de INSTALLMESSAGE \_**
</dt> <dd>

Mensagem de erro formatada.

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**aviso de INSTALLMESSAGE \_**
</dt> <dd>

Mensagem de aviso formatada.

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**informações de INSTALLMESSAGE \_**
</dt> <dd>

Mensagem de log formatada.

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_usuário INSTALLMESSAGE**
</dt> <dd>

Mensagem de usuário formatada.

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**
</dt> <dd>

Mensagem formatada indicando uma condição de espaço em disco insuficiente

</dd> </dl>

O manipulador de usuário externo pode usar as seguintes Windows Installer mensagens para monitorar uma sequência da interface do usuário do Windows Installer. O instalador envia essas mensagens no início de uma sequência de interface do usuário Windows Installer, uma vez que cada caixa de diálogo é exibida e no final da sequência da interface do usuário. Nenhum processamento é necessário para usar essas mensagens.

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ encerrar
</dt> <dd>

Essa mensagem indica o final da sequência da interface do usuário. A cadeia de caracteres é uma cadeia de caracteres nula.

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE \_ inicializar
</dt> <dd>

Essa mensagem indica que a sequência da interface do usuário foi iniciada. A cadeia de caracteres é uma cadeia de caracteres nula.

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG
</dt> <dd>

A cadeia de caracteres contém o nome da caixa de diálogo atual.

</dd> </dl>

As mensagens de Windows Installer a seguir exigem processamento adicional pelo manipulador de interface do usuário externa.

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ resolver**
</dt> <dd>

O manipulador de interface do usuário externo deve retornar 0 e permitir que Windows Installer manipule a mensagem. O manipulador de interface do usuário externo pode monitorar essa mensagem, mas não deve executar nenhuma ação que afete a instalação.

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**
</dt> <dd>

A interface do usuário externa deve exibir uma [caixa de diálogo FilesInUse](filesinuse-dialog.md) em resposta a esta mensagem.

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**
</dt> <dd>

A interface do usuário externa deve exibir uma [caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) em resposta a esta mensagem. Disponível a partir do Windows Installer versão 4,0. Para obter mais informações sobre essa mensagem, consulte [usando o Gerenciador de reinicialização com uma interface do usuário externa](using-restart-manager-with-an-external-ui-.md).

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**
</dt> <dd>

Essa mensagem fornece informações sobre a ação atual. O formato é a ação \[ 1 \] : \[ 2 \] . \[3 \] , em que um dois-pontos é usado para separar o campo 1 e o campo 2 e um ponto é usado para separar o campo 2 e o campo 3. O campo \[ 1 \] contém a hora em que a ação foi iniciada usando o formato de propriedade [**time**](time.md) . O campo \[ 2 \] contém o nome da ação da tabela de sequência. \[O campo 3 \] fornece a descrição da ação da [tabela ActionText](actiontext-table.md) ou da função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**
</dt> <dd>

O formato dessa cadeia de caracteres é especificado pelo valor do [modelo](template.md) fornecido na [tabela ActionText](actiontext-table.md) ou pela função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Pode haver um número ilimitado de mensagens **INSTALLMESSAGE \_ ACTIONDATA** após a mensagem **INSTALLMESSAGE \_ ACTIONSTART** .

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**
</dt> <dd>

Esta mensagem tem três subtipos: idioma, legenda e CancelShow. A cadeia de caracteres pode ter três campos delimitados por um número seguido por dois-pontos. Nem todos os campos são obrigatórios. A mensagem pode ser uma cadeia de caracteres nula ou vazia ("").

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

O campo 1 contém o valor 0 para indicar que esta cadeia de caracteres contém informações de idioma. O campo 2 contém um valor de [idioma](language.md) que é um identificador de idioma numérico (LangID). O campo 3 é um valor que representa uma página de código ANSI.

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Legenda
</dt> <dd>

O campo 1 contém o valor 1 para indicar que esta cadeia de caracteres contém o texto de uma legenda ou título. O campo 2 contém texto que um manipulador de interface de usuário externa pode usar como uma legenda de título para uma caixa de diálogo. O campo 3 é nulo ou uma cadeia de caracteres vazia (""). O campo 3 pode estar ausente em uma mensagem de legenda.

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow
</dt> <dd>

O campo 1 contém o valor 2 para indicar que essa cadeia de caracteres contém informações sobre se o botão Cancelar deve ser exibido. Se o botão Cancelar estiver oculto, o campo 2 conterá o valor 0. Se o botão Cancelar estiver visível, o campo 2 conterá o valor 1.

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progresso do INSTALLMESSAGE \_
</dt> <dd>

Esta mensagem tem quatro subtipos: redefinir, ActionInfo, ProgressReport e ProgressAddition. O manipulador externo não deve agir sobre nenhuma dessas mensagens até que a primeira mensagem de progresso de redefinição seja recebida. Isso fornece uma estimativa do número total de tiques para a barra de progresso.

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Definido
</dt> <dd>

O campo 1 contém o valor 0 para indicar uma redefinição da barra de progresso. O campo 2 contém o número total de tiques na barra de progresso. O campo 3 contém o valor 0 para o movimento de barra de progresso de encaminhamento. O campo 3 contém o valor 1 para o movimento de barra de progresso regressivo. O valor 0 no campo 4 significa que a instalação está em andamento e o tempo restante pode ser calculado. O valor 1 no campo 4 significa que o script está sendo executado e "Aguarde..." a mensagem pode ser exibida. A estimativa do número total de tiques é uma aproximação e pode ser imprecisa.

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo
</dt> <dd>

O campo 1 contém o valor 1 para indicar que esta cadeia de caracteres contém informações de ação. O campo 2 contém o número de tiques que a barra de progresso move para cada mensagem ActionData enviada pela ação atual. Se o campo 3 contiver o valor 0, ignore o campo 2. Se o campo 3 contiver o valor 1, aumente a barra de progresso pelo número de tiques no campo 2 para cada mensagem ActionData enviada pela ação atual. O campo 4 não é usado.

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport
</dt> <dd>

O campo 1 contém o valor 2 para indicar que essa cadeia de caracteres contém informações de progresso. O campo 2 contém o número de tiques que a barra de progresso moveu. O campo 3 não é usado. O campo 4 não é usado.

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition
</dt> <dd>

O campo 1 contém o valor 3 para indicar que uma ação pode adicionar tiques à barra de progresso. O campo 2 contém o número de tiques a serem adicionados à contagem total esperada de tiques de progresso. O campo 3 não é usado. O campo 4 não é usado.

</dd> </dl> </dd> </dl>

 

 



