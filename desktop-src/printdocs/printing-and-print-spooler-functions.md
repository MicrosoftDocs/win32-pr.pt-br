---
description: A API spooler de impressão contém as funções e estruturas de dados que os aplicativos usam para gerenciar o spooler de impressão do Windows e as impressoras e os trabalhos de impressão que ele controla.
ms.assetid: d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39
title: Funções da API do Spooler de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df751b11206ebf26d2d0e8fd88f61ede8447dad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171593"
---
# <a name="print-spooler-api-functions"></a>Funções da API do Spooler de impressão

A API spooler de impressão contém as funções e estruturas de dados que os aplicativos usam para gerenciar o spooler de impressão do Windows e as impressoras e os trabalhos de impressão que ele controla.

As funções da API spooler de impressão são divididas nos seguintes grupos:

-   [Funções de trabalho de impressão](#print-job-functions)
-   [Funções da interface do usuário da impressora](#printer-user-interface-functions)
-   [Funções de impressora](#printer-functions)
-   [Funções de notificação de alteração de impressora](#printer-change-notification-functions)
-   [Funções de formulário de impressora](#printer-form-functions)
-   [Funções de spooler de impressão](#print-spooler-api-functions)

## <a name="print-job-functions"></a>Funções de trabalho de impressão

Essas funções enviam trabalhos de impressão para uma impressora e rastreiam e controlam os trabalhos de impressão no spooler de impressão.



| Função                                                                      | Descrição                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddJob**](addjob.md)<br/>                                           | A função [**AddJob**](/windows/desktop/printdocs/addjob) adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho. <br/>                                      |
| [**ClosePrinter**](closeprinter.md)<br/>                               | A função [**ClosePrinter**](/windows/desktop/printdocs/closeprinter) fecha o objeto de impressora especificado. <br/>                                                                                                                                                      |
| [**DocumentEvent**](documentevent.md)<br/>                             | A função [**DocumentEvent**](/windows/desktop/printdocs/documentevent) é um manipulador de eventos para eventos associados à impressão de um documento. <br/>                                                                                                                     |
| [**DocumentProperties**](documentproperties.md)<br/>                   | A função [**DocumentProperties**](/windows/desktop/printdocs/documentproperties) recupera ou modifica informações de inicialização de impressora ou exibe uma folha de propriedades de configuração de impressora para a impressora especificada. <br/>                                        |
| [**EndDocPrinter**](enddocprinter.md)<br/>                             | A função [**EndDocPrinter**](/windows/desktop/printdocs/enddocprinter) encerra um trabalho de impressão para a impressora especificada. <br/>                                                                                                                                             |
| [**EndPagePrinter**](endpageprinter.md)<br/>                           | A função [**EndPagePrinter**](/windows/desktop/printdocs/endpageprinter) notifica o spooler de impressão que o aplicativo está no final de uma página em um trabalho de impressão. <br/>                                                                                               |
| [**EnumJobs**](enumjobs.md)<br/>                                       | A função [**EnumJobs**](/windows/desktop/printdocs/enumjobs) recupera informações sobre um conjunto especificado de trabalhos de impressão para uma impressora especificada. <br/>                                                                                                                |
| [**GetJob**](getjob.md)<br/>                                           | A função [**GetJob**](/windows/desktop/printdocs/getjob) recupera informações sobre um trabalho de impressão especificado. <br/>                                                                                                                                                    |
| [**OpenPrinter**](openprinter.md)<br/>                                 | A função [**OpenPrinter**](/windows/desktop/printdocs/openprinter) recupera um identificador para a impressora ou o servidor de impressão especificado ou outros tipos de identificadores no subsistema de impressão. <br/>                                                                               |
| [**OpenPrinter2**](openprinter2.md)<br/>                               | Recupera um identificador para a impressora especificada, o servidor de impressão ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora.<br/>                                                                                      |
| [**ReportJobProcessingProgress**](reportjobprocessingprogress.md)<br/> | Relata para o serviço spooler de impressão se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização e qual parte do processamento está em andamento no momento.<br/>                                                                               |
| [**ScheduleJob**](schedulejob.md)<br/>                                 | A função [**ScheduleJob**](/windows/desktop/printdocs/schedulejob) solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão. <br/>                                                                                                                |
| [**SetJob**](setjob.md)<br/>                                           | A função [**SetJob**](/windows/desktop/printdocs/setjob) pausa, retoma, cancela ou reinicia um trabalho de impressão em uma impressora especificada. Você também pode usar a função **SetJob** para definir parâmetros de trabalho de impressão, como a prioridade do trabalho de impressão e o nome do documento. <br/> |
| [**StartDocPrinter**](startdocprinter.md)<br/>                         | A função [**StartDocPrinter**](/windows/desktop/printdocs/startdocprinter) notifica o spooler de impressão de que um documento deve ser colocado no spool para impressão. <br/>                                                                                                           |
| [**StartPagePrinter**](startpageprinter.md)<br/>                       | A função [**StartPagePrinter**](/windows/desktop/printdocs/startpageprinter) notifica o spooler de que uma página está prestes a ser impressa na impressora especificada. <br/>                                                                                                 |



 

## <a name="printer-user-interface-functions"></a>Funções da interface do usuário da impressora

Essas funções exibem uma interface do usuário que permite ao usuário selecionar ou configurar uma impressora.



| Função                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedDocumentProperties**](advanceddocumentproperties.md)<br/> | A função [**AdvancedDocumentProperties**](/windows/desktop/printdocs/advanceddocumentproperties) exibe uma caixa de diálogo de configuração de impressora para a impressora especificada, permitindo que o usuário configure essa impressora. <br/>                                                                                                                                                      |
| [**ConfigurePort**](configureport.md)<br/>                           | A função [**ConfigurePort**](/windows/desktop/printdocs/configureport) exibe a caixa de diálogo porta-configuração de uma porta no servidor especificado. <br/>                                                                                                                                                                                                                     |
| [**ConnectToPrinterDlg**](connecttoprinterdlg.md)<br/>               | A função [**ConnectToPrinterDlg**](/windows/desktop/printdocs/connecttoprinterdlg) exibe uma caixa de diálogo que permite aos usuários navegar e se conectar a impressoras em uma rede. Se o usuário selecionar uma impressora, a função tentará criar uma conexão a ela; se um driver adequado não estiver instalado no servidor, o usuário terá a opção de criar uma impressora localmente. <br/> |
| [**Impressoras**](printerproperties.md)<br/>                   | A função [**impressorasproperties**](/windows/desktop/printdocs/printerproperties) exibe uma folha de propriedades da impressora para a impressora especificada. <br/>                                                                                                                                                                                                                    |



 

## <a name="printer-functions"></a>Funções de impressora

Essas funções adicionam e configuram as impressoras que o spooler de impressão usa.



| Função                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPrinter**](abortprinter.md)<br/>                       | A função [**AbortPrinter**](/windows/desktop/printdocs/abortprinter) excluirá o arquivo de spool de uma impressora se a impressora estiver configurada para o spool. <br/>                                                                                                                                                                                                                                                                  |
| [**AddPrinter**](addprinter.md)<br/>                           | A função [**AddPrinter**](/windows/desktop/printdocs/addprinter) adiciona uma impressora à lista de impressoras com suporte para um servidor especificado. <br/>                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection**](addprinterconnection.md)<br/>       | A função **AddPrinterConnection** adiciona uma conexão à impressora especificada para o usuário atual. <br/>                                                                                                                                                                                                                                                                                       |
| [**AddPrinterConnection2**](addprinterconnection2.md)<br/>     | Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.<br/>                                                                                                                                                                                                                                                                                             |
| [**DeletePrinter**](deleteprinter.md)<br/>                     | A função [**DeletePrinter**](/windows/desktop/printdocs/deleteprinter) exclui o objeto de impressora especificado. <br/>                                                                                                                                                                                                                                                                                                    |
| [**DeletePrinterConnection**](deleteprinterconnection.md)<br/> | A função [**DeletePrinterConnection**](/windows/desktop/printdocs/deleteprinterconnection) exclui uma conexão a uma impressora que foi estabelecida por uma chamada para [**AddPrinterConnection**](addprinterconnection.md) ou [**ConnectToPrinterDlg**](connecttoprinterdlg.md). <br/>                                                                                                                                      |
| [**DeletePrinterData**](deleteprinterdata.md)<br/>             | A função [**DeletePrinterData**](/windows/desktop/printdocs/deleteprinterdata) exclui os dados de configuração especificados para uma impressora. Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados. A função **DeletePrinterData** exclui um desses valores, especificados por seu nome de valor. <br/>                                                                                                     |
| [**DeletePrinterDataEx**](deleteprinterdataex.md)<br/>         | A função [**DeletePrinterDataEx**](/windows/desktop/printdocs/deleteprinterdataex) exclui um valor especificado dos dados de configuração para uma impressora. Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados armazenados em uma hierarquia de chaves do registro. A função exclui um valor especificado em uma chave especificada. <br/>                                                                        |
| [**DeletePrinterKey**](deleteprinterkey.md)<br/>               | A função [**DeletePrinterKey**](/windows/desktop/printdocs/deleteprinterkey) exclui uma chave especificada e todas as suas subchaves para uma impressora especificada. <br/>                                                                                                                                                                                                                                                               |
| [**EnumPrinterData**](enumprinterdata.md)<br/>                 | A função [**EnumPrinterData**](/windows/desktop/printdocs/enumprinterdata) enumera dados de configuração para uma impressora especificada. <br/>                                                                                                                                                                                                                                                                               |
| [**EnumPrinterDataEx**](enumprinterdataex.md)<br/>             | A função [**EnumPrinterDataEx**](/windows/desktop/printdocs/enumprinterdataex) enumera todos os nomes de valor e dados para uma impressora e chave especificadas. <br/>                                                                                                                                                                                                                                                             |
| [**EnumPrinterKey**](enumprinterkey.md)<br/>                   | A função [**EnumPrinterKey**](/windows/desktop/printdocs/enumprinterkey) enumera as subchaves de uma chave especificada para uma impressora especificada. <br/>                                                                                                                                                                                                                                                                     |
| [**EnumPrinters**](enumprinters.md)<br/>                       | A função [**EnumPrinters**](/windows/desktop/printdocs/enumprinters) enumera impressoras disponíveis, servidores de impressão, domínios ou provedores de impressão. <br/>                                                                                                                                                                                                                                                                 |
| [**FlushPrinter**](flushprinter.md)<br/>                       | A função [**FlushPrinter**](/windows/desktop/printdocs/flushprinter) envia um buffer para a impressora a fim de limpá-lo de um estado transitório. <br/>                                                                                                                                                                                                                                                                 |
| [**GetDefaultPrinter**](getdefaultprinter.md)<br/>             | A função [**GetDefaultPrinter**](/windows/desktop/printdocs/getdefaultprinter) recupera o nome da impressora padrão para o usuário atual no computador local. <br/>                                                                                                                                                                                                                                    |
| [**Getprinter**](getprinter.md)<br/>                           | A função [**Getprinter**](/windows/desktop/printdocs/getprinter) recupera informações sobre uma impressora especificada. <br/>                                                                                                                                                                                                                                                                                               |
| [**GetPrinterData**](getprinterdata.md)<br/>                   | A função [**GetPrinterData**](/windows/desktop/printdocs/getprinterdata) recupera dados de configuração para a impressora ou o servidor de impressão especificado. <br/>                                                                                                                                                                                                                                                                |
| [**GetPrinterDataEx**](getprinterdataex.md)<br/>               | A função [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) recupera dados de configuração para a impressora ou o servidor de impressão especificado. **GetPrinterDataEx** pode recuperar valores armazenados pela função [**SetPrinterData**](setprinterdata.md) . Além disso, o **GetPrinterDataEx** pode recuperar valores armazenados em uma chave especificada pela função [**SetPrinterDataEx**](setprinterdataex.md) . <br/> |
| [**IsValidDevmode**](isvaliddevmode.md)<br/>                   | A função [**IsValidDevmode**](isvaliddevmode.md) verifica se o conteúdo de uma estrutura DEVMODE é válido. <br/>                                                                                                                                                                                                                                                                           |
| [**ReadPrinter**](readprinter.md)<br/>                         | A função [**ReadPrinter**](/windows/desktop/printdocs/readprinter) recupera dados da impressora especificada. <br/>                                                                                                                                                                                                                                                                                                   |
| [**ResetPrinter**](resetprinter.md)<br/>                       | A função [**ResetPrinter**](/windows/desktop/printdocs/resetprinter) especifica o tipo de dados e os valores do modo de dispositivo a serem usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) . Esses valores podem ser substituídos usando a função [**SetJob**](setjob.md) após o início da impressão do documento. <br/>                                                                  |
| [**SetDefaultPrinter**](setdefaultprinter.md)<br/>             | A função [**SetDefaultPrinter**](/windows/desktop/printdocs/setdefaultprinter) define o nome da impressora padrão para o usuário atual no computador local. <br/>                                                                                                                                                                                                                                         |
| [**SetPort**](setport.md)<br/>                                 | A função [**SetPort**](/windows/desktop/printdocs/setport) define o status associado a uma porta de impressora. <br/>                                                                                                                                                                                                                                                                                                      |
| [**Setprinter**](setprinter.md)<br/>                           | A função [**Setprinter**](/windows/desktop/printdocs/setprinter) define os dados de uma impressora especificada ou define o estado da impressora especificada pausando a impressão, retomando a impressão ou limpando todos os trabalhos de impressão. <br/>                                                                                                                                                                                           |
| [**SetPrinterData**](setprinterdata.md)<br/>                   | A função [**SetPrinterData**](/windows/desktop/printdocs/setprinterdata) define os dados de configuração para um servidor de impressão ou impressora. <br/>                                                                                                                                                                                                                                                                             |
| [**SetPrinterDataEx**](setprinterdataex.md)<br/>               | A função [**SetPrinterDataEx**](/windows/desktop/printdocs/setprinterdataex) define os dados de configuração para um servidor de impressão ou impressora. A função armazena os dados de configuração na chave do registro da impressora. <br/>                                                                                                                                                                                            |
| [**WritePrinter**](writeprinter.md)<br/>                       | A função [**WritePrinter**](writeprinter.md) notifica o spooler de impressão que os dados devem ser gravados na impressora especificada. <br/>                                                                                                                                                                                                                                                           |



 

## <a name="printer-change-notification-functions"></a>Funções de notificação de alteração de impressora

Essas funções permitem que um aplicativo seja notificado sobre alterações no status de uma impressora.



| Função                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md)<br/> | A função [**FindClosePrinterChangeNotification**](/windows/desktop/printdocs/findcloseprinterchangenotification) fecha um objeto de notificação de alteração criado chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . A impressora ou o servidor de impressão associado ao objeto de notificação de alteração não será mais monitorado por esse objeto. <br/> |
| [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)<br/> | A função [**FindFirstPrinterChangeNotification**](/windows/desktop/printdocs/findfirstprinterchangenotification) cria um objeto de notificação de alteração e retorna um identificador para o objeto. Você pode usar esse identificador em uma chamada para uma das funções de espera para monitorar as alterações na impressora ou no servidor de impressão. <br/>                                                                              |
| [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)<br/>   | A função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) recupera informações sobre a notificação de alteração mais recente para um objeto de notificação de alteração associado a um servidor de impressão ou impressora. Chame essa função quando uma operação de espera no objeto de notificação de alteração for satisfeita. <br/>                                           |
| [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md)<br/>                           | A função [**FreePrinterNotifyInfo**](/windows/desktop/printdocs/freeprinternotifyinfo) libera um buffer alocado pelo sistema criado pela função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . <br/>                                                                                                                                                                |



 

## <a name="printer-form-functions"></a>Funções de formulário de impressora

Essas funções gerenciam os formulários usados por uma impressora.



| Função                                    | Descrição                                                                                                                                    |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddFormat**](addform.md)<br/>       | A função [**AddFormat**](/windows/desktop/printdocs/addform) adiciona um formulário à lista de formulários disponíveis que podem ser selecionados para a impressora especificada. <br/> |
| [**DeleteForm**](deleteform.md)<br/> | A função [**DeleteForm**](/windows/desktop/printdocs/deleteform) remove um nome de formulário da lista de formulários com suporte. <br/>                                |
| [**EnumForms**](enumforms.md)<br/>   | A função [**EnumForms**](/windows/desktop/printdocs/enumforms) enumera os formulários com suporte na impressora especificada. <br/>                               |
| [**GetForm**](getform.md)<br/>       | A função [**GetForm**](/windows/desktop/printdocs/getform) recupera informações sobre um formulário especificado. <br/>                                              |
| [**Formulário**](setform.md)<br/>       | A função [**setform**](/windows/desktop/printdocs/setform) define as informações do formulário para a impressora especificada. <br/>                                       |



 

## <a name="print-spooler-functions"></a>Funções de spooler de impressão

Essas funções interagem com o spooler de impressão em um nível baixo.



| Função                                                          | Descrição                                                                                                                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseSpoolFileHandle**](closespoolfilehandle.md)<br/>   | A função [**CloseSpoolFileHandle**](/windows/desktop/printdocs/closespoolfilehandle) fecha um identificador para um arquivo de spool associado ao trabalho de impressão atualmente enviado pelo aplicativo. <br/>                    |
| [**CommitSpoolData**](commitspooldata.md)<br/>             | A função [**CommitSpoolData**](/windows/desktop/printdocs/commitspooldata) notifica o spooler de impressão que uma quantidade especificada de dados foi gravada em um arquivo de spool especificado e está pronta para ser renderizada. <br/> |
| [**GetPrintExecutionData**](getprintexecutiondata.md)<br/> | O [**GetPrintExecutionData**](getprintexecutiondata.md) recupera o contexto de impressão atual.<br/>                                                                                             |
| [**GetSpoolFileHandle**](getspoolfilehandle.md)<br/>       | A função [**GetSpoolFileHandle**](/windows/desktop/printdocs/getspoolfilehandle) recupera um identificador para o arquivo de spool associado ao trabalho enviado no momento pelo aplicativo. <br/>                        |



 

 

