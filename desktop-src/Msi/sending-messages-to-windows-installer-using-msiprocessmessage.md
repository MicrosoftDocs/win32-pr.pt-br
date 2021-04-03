---
description: As mensagens enviadas usando MsiProcessMessage são as mesmas mensagens que são recebidas pela \_ função de retorno de chamada do manipulador INSTALLUI se MsiSetExternalUI foi chamado.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Enviar mensagens para Windows Installer usando o MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922806"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a>Enviando mensagens para Windows Installer usando o MsiProcessMessage

As mensagens enviadas usando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) são as mesmas mensagens que são recebidas pela função de retorno de chamada do [**\_ manipulador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) se [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) foi chamado. Caso contrário, Windows Installer tratar as mensagens. Para obter detalhes, consulte [analisando mensagens de Windows Installer](parsing-windows-installer-messages.md).

Por exemplo, para enviar uma \_ mensagem de erro INSTALLMESSAGE com o \_ ícone MB ICONWARNING e os \_ botões MB ABORTRETRYCANCEL:


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



Em que *hInstall* é o identificador para a instalação, fornecido a uma ação personalizada ou ao identificador *hProduct* de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), e *hRec* é o registro que contém as informações de erro a serem formatadas. Para obter informações sobre como a formatação é executada, consulte [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).

Por padrão, se uma \_ mensagem de erro INSTALLMESSAGE ou INSTALLMESSAGE \_ FATALEXIT for enviada sem especificar tipos de botão ou de ícone, MB \_ OK, nenhum ícone e MB \_ DEFBUTTON1 serão usados.

Windows Installer não rotula o botão **abortar** com a cadeia de caracteres "Abort" ao exibir uma MessageBox com a \_ especificação do botão MB ABORTRETRYIGNORE, em vez disso, ela rotula o botão com a cadeia de caracteres "Cancel". Todas as mensagens de erro evitem usar a palavra "Abort" e, em vez disso, usar a palavra "Cancel".

O parâmetro *hRecord* da função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) depende do tipo de mensagem enviado para o [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). A lista a seguir detalha os requisitos do registro em relação ao tipo de mensagem:

INSTALLMESSAGE \_ FATALEXIT

 

informações de INSTALLMESSAGE \_

 

INSTALLMESSAGE \_ OUTOFDISKSPACE



| Campo         | Descrição                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | Modelo para a formatação da cadeia de caracteres resultante. Consulte [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) para obter mais informações. Os campos do registro são referenciados usando \[ 1 \] para o campo 1, \[ 2 \] para o campo 2, etc. |
| 1 a *n* | Todos os campos subsequentes estão diretamente relacionados aos campos referenciados pelo modelo no campo 0.                                                                                                                    |



 

Se o campo 0 for nulo, a cadeia de caracteres recebida pelo manipulador de interface do usuário será formatada como: 1: \[ dados do campo 1 \] 2: \[ dados do campo 2, \] o que significa que, para cada campo do registro, a cadeia de caracteres contém o número do campo seguido pelos dados armazenados no campo.

As mensagens de informações de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) são registradas quando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), a [opção de linha de comando](command-line-options.md)'/l ' ou a [política de registro](logging.md) especifica ' I ' ou informações de INSTALLLOGMODE \_ .

erro de INSTALLMESSAGE \_

 

aviso de INSTALLMESSAGE \_

 

\_usuário INSTALLMESSAGE

Para usar uma mensagem da tabela de erros.



| Campo         | Descrição                                           |
|---------------|-------------------------------------------------------|
| 0             | Deve ser NULL.                                         |
| 1             | Número da mensagem na [tabela de erros](error-table.md). |
| 2 a *n* | Relacionado à mensagem especificada na tabela de erros.  |



 

Por exemplo.



| Campo | Tipo   | Dados       |
|-------|--------|------------|
| 0     | string | nulo       |
| 1     | INT    | 1304       |
| 2     | string | Myfile.txt |



 

A mensagem resultante recebida do manipulador de interface do usuário é:

Erro 1304. Erro ao gravar no arquivo: Myfile.txt. Verifique se você tem acesso a esse diretório.

Se o campo 0 não for nulo, a mensagem da tabela de erros será substituída. Em vez disso, o modelo campo 0 determina o formato da mensagem.

A mensagem também pode especificar os botões, incluindo o botão padrão e o ícone a ser usado com a mensagem, conforme mencionado acima. Os tipos de botão e ícone são listados [**no \_ manipulador INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).

INSTALLMESSAGE \_ COMMONDATA

Essa mensagem é enviada para habilitar ou desabilitar o botão **Cancelar** em uma caixa de diálogo de progresso.



| Campo | Descrição                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Não utilizado.                                                                                                                                      |
| 1     | 2 refere-se ao botão **Cancelar** .                                                                                                           |
| 2     | Um valor de 1 indica que o botão de **cancelamento** deve estar visível. Um valor de 0 indica que o botão de **cancelamento** deve ser invisível.<br/> |



 

Por exemplo, para desabilitar ou ocultar o botão **Cancelar** , o registro seria exibido da seguinte maneira.



| Campo | Tipo   | Dados |
|-------|--------|------|
| 0     | string | nulo |
| 1     | INT    | 2    |
| 2     | INT    | 0    |



 

INSTALLMESSAGE \_ ACTIONSTART

 

INSTALLMESSAGE \_ ACTIONDATA

O \_ registro INSTALLMESSAGE ACTIONSTART determina o formato do registro ActionData.



| Campo | Descrição                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| 0     | nulo                                                                                                          |
| 1     | Nome da ação. O nome neste campo deve ser não nulo.                                                         |
| 2     | Descrição da ação.                                                                                           |
| 3     | Modelo de ação. Isso é usado para o ActionData cuja mensagem está sendo formatada de acordo com este modelo. |



 

Não referencie o campo 0 na mensagem do modelo de ação.

O \_ registro INSTALLMESSAGE ACTIONDATA é formatado da seguinte maneira.



| Campo         | Descrição                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0             | nulo                                                                                                                                               |
| 1 a *n* | Dependendo do campo 3 da \_ mensagem ou do modelo ACTIONSTART INSTALLMESSAGE correspondente especificado na [tabela ActionText](actiontext-table.md). |



 

Por exemplo, o \_ registro INSTALLMESSAGE ACTIONSTART.



| Campo | Tipo   | Dados                                                            |
|-------|--------|-----------------------------------------------------------------|
| 0     | string | nulo                                                            |
| 1     | string | Myaction                                                        |
| 2     | string | Esta é a descrição de "myaction"                           |
| 3     | string | Modelo myaction: os dados de field1 são \[ 1 \] . os dados do campo 2 são \[ 2 \] . |



 

O modelo para INSTALLMESSAGE \_ ACTIONSTART (campo 3) faz referência aos campos 1 e 2, o registro de ACTIONDATA de INSTALLMESSAGE \_ deve ter dois campos contendo os dados garantidos. Os campos podem ser campos de cadeia de caracteres ou inteiros.

\_Registro de ACTIONDATA INSTALLMESSAGE.



| Campo | Tipo   | Dados                    |
|-------|--------|-------------------------|
| 0     | string | nulo                    |
| 1     | INT    | 2                       |
| 2     | string | ActionData para myaction |



 

INSTALLMESSAGE \_ FILESINUSE

O registro FILESINUSE é um registro de comprimento variável.



| Campo | Descrição                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Este campo pode ser nulo. Para uma instalação usando uma interface do usuário básica, esse campo pode especificar texto estático para exibição no [controle ListBox](listbox-control.md) da [caixa de diálogo FilesInUse](filesinuse-dialog.md). Para uma instalação usando uma interface do usuário completa, esse campo não tem efeito porque o texto é especificado pela criação da caixa de diálogo FilesInUse personalizada. |
| 1     | Nome do arquivo em uso.                                                                                                                                                                                                                                                                                                                                        |
| 2     | Este campo identifica o processo que contém o arquivo em uso. **Windows Installer versão 4,0:** A ID do processo (PID) do processo ou o título da janela do processo.<br/> **Windows Installer versão 3,1 e anteriores:** Esse campo deve ser a identificação do processo (PID) do processo.<br/>                                                      |



 

Por exemplo, para enviar uma mensagem FilesInUse mostrando dois arquivos em uso, red.exe e blue.exe, o registro tem quatro campos mais o campo 0. O formato do registro seria como mostrado na tabela a seguir. Este exemplo requer Windows Installer versão 4,0.

**Windows Installer versão 3,1 e anteriores:** Os campos 2 e 4 no exemplo a seguir devem conter os PIDs dos processos que mantêm red.exe e blue.exe em uso.



| Campo | Descrição       |
|-------|-------------------|
| 0     | nulo              |
| 1     | Red.exe           |
| 2     | Título da janela vermelha  |
| 3     | Blue.exe          |
| 4     | Título da janela azul |



 

> [!Note]  
> No Windows Installer versão 4,0, se a PID passada do serviço não tiver um título de janela, como um aplicativo de bandeja do sistema, o arquivo não será exibido e o log detalhado conterá as mensagens a seguir.

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

INSTALLMESSAGE \_ resolver

O \_ registro de resolução INSTALLMESSAGE tem sete campos. Para \_ que o resolvedor de INSTALLMESSAGE funcione corretamente, um manipulador de interface do usuário externa pode não manipular a \_ mensagem de resolução INSTALLMESSAGE. Windows Installer deve manipular a \_ mensagem de resolução INSTALLMESSAGE. Ou seja, o manipulador de interface do usuário externa retorna 0 para indicar "nenhuma ação tomada" ao filtrar a \_ mensagem de resolução INSTALLMESSAGE. A prática recomendada é evitar o envio de uma mensagem de resolução.



| Campo | Descrição                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | nulo                                                                                                                                                               |
| 1     | null                                                                                                                                                               |
| 2     | Nome do pacote.                                                                                                                                                      |
| 3     | Código do produto.                                                                                                                                                      |
| 4     | O caminho relativo, se conhecido, pode ser nulo.                                                                                                                               |
| 5     | 0                                                                                                                                                                  |
| 6     | Se o código do pacote deve ser validado. Um valor de ' 1 ' indica que o código do pacote deve ser validado. Um valor de ' 0 ' indica que o pacote não deve ser validado. |
| 7     | Disco necessário da tabela de mídia. Um valor de ' 0 ' indica que qualquer disco é aceitável.                                                                              |



 

 

 




