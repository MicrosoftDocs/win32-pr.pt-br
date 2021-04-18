---
description: Lista as interfaces de programação de aplicativo (APIs) de impressão introduzidas no Windows Vista.
ms.assetid: 7a4eb5d7-b37d-4090-aea4-7274daa1e15c
title: O que há de novo para impressão no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8648d57f48623e6db0f6311bb07ae24ac15d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798553"
---
# <a name="whats-new-for-printing-in-windows-vista"></a>O que há de novo para impressão no Windows Vista

Lista as interfaces de programação de aplicativo (APIs) de impressão introduzidas no Windows Vista.

As seguintes funções e enumerações são usadas para gerenciar tíquetes de impressão.



| Função                                                               | Descrição                                                                                                                                   | Cabeçalho    | Biblioteca     |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------|
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) | Converte um tíquete de impressão em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) | Converte um [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) em um tíquete de impressão.                                                                                      | Prntvpt. h | Prntvpt. lib |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)                             | Libera buffers criados por determinadas funções de gerenciamento de tíquete de impressão.                                                                        | Prntvpt. h | Prntvpt. lib |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) | Valida e mescla dois tíquetes de impressão em um tíquete de impressão viável.                                                                            | Prntvpt. h | Prntvpt. lib |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)               | Obtém uma conta dos recursos da impressora.                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)                               | Abre um provedor de tíquete de impressão.                                                                                                                | Prntvpt. h | Prntvpt. lib |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)                           | Abre um provedor de tíquete de impressão, mesmo que ele não ofereça suporte à versão preferencial do [esquema de impressão](./print-schema.md). | Prntvpt. h | Prntvpt. lib |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)                             | Fecha um provedor de tíquete de impressão.                                                                                                               | Prntvpt. h | Prntvpt. lib |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)     | Obtém a versão mais recente do [esquema de impressão](./print-schema.md) compatível com uma impressora especificada.                        | Prntvpt. h | Prntvpt. lib |



 



| Enumeração                                        | Descrição                                                                                                                                                                               | Cabeçalho    |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) | Permite que os chamadores especifiquem qual [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) é usado como a fonte de valores padrão quando um tíquete de impressão não especifica todas as configurações que podem estar em um **DEVMODE**. | Prntvpt. h |
| [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope)     | Especifica o escopo de um tíquete de impressão.                                                                                                                                                    | Prntvpt. h |



 

As funções a seguir são usadas para instalar drivers de impressora.



| Função                                                                   | Descrição                                                                                                                                                                 | Cabeçalho     | Biblioteca      |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CorePrinterDriverInstalled**](coreprinterdriverinstalled.md)           | Relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.                                                                                | Winspool. h | Winspool. lib |
| [**DeletePrinterDriverPackage**](deleteprinterdriverpackage.md)           | Exclui um pacote de driver de impressora do repositório de drivers.                                                                                                                     | Winspool. h | Winspool. lib |
| [**GetCorePrinterDrivers**](getcoreprinterdrivers.md)                     | Obtém o GUID, a versão e a data dos drivers de impressora principal especificados e o caminho para seus pacotes.                                                                      | Winspool. h | Winspool. lib |
| [**GetPrinterDriverPackagePath**](getprinterdriverpackagepath.md)         | Obtém o caminho para o pacote de driver de impressora especificado em um servidor de impressão.                                                                                                    | Winspool. h | Winspool. lib |
| [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) | Instala um driver de impressora de um pacote de driver no repositório de drivers do servidor de impressão.                                                                                         | Winspool. h | Winspool. lib |
| [**UploadPrinterDriverPackage**](uploadprinterdriverpackage.md)           | Carrega um driver de impressora no repositório de drivers de um servidor de impressão para que ele possa ser instalado com o [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md). | Winspool. h | Winspool. lib |



 

As seguintes funções, enumerações e estruturas são usadas para imprimir e gerenciar impressoras e conexões de impressora.



| Função                                               | Descrição                                                                                                                                              | Cabeçalho     | Biblioteca      |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**AddPrinterConnection2**](addprinterconnection2.md) | Adiciona uma conexão à impressora especificada para o usuário atual.                                                                                         | Winspool. h | Winspool. lib |
| [**OpenPrinter2**](openprinter2.md)                   | Recupera um identificador para a impressora ou o servidor de impressão especificado, ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora. | Winspool. h | Winspool. lib |



 



| Enumeração                                            | Descrição                                                                                       | Cabeçalho     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------|------------|
| [**\_sinalizadores de opção de impressora \_**](printer-option-flags.md) | Especifica o cache de um identificador para uma impressora aberta com [**OpenPrinter2**](openprinter2.md). | Winspool. h |



 



| Estrutura                                                         | Descrição                                                                            | Cabeçalho     |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------|
| [**\_Driver de impressora principal \_**](core-printer-driver.md)              | Representa um driver de impressora no qual os outros drivers de impressora são dependentes.              | Winspool. h |
| [**Informações do DRIVER \_ \_ 8**](driver-info-8.md)                          | Representa um driver de impressora.                                                           | Winspool. h |
| [**Informações do formulário \_ \_ 2**](form-info-2.md)                              | Representa informações sobre um formulário de impressão localizável.                                 | Winspool. h |
| [**Informações do trabalho \_ \_ 4**](job-info-4.md)                                | Representa um conjunto completo de valores associados a um trabalho e dá suporte a arquivos de spool de 64 bits. | Winspool. h |
| [**Informações de conexão da impressora \_ \_ \_ 1**](printer-connection-info-1.md) | Representa informações sobre uma conexão a uma impressora.                                | Winspool. h |
| [**opções de impressora \_**](printer-options.md)                       | Representa opções de impressora.                                                            | Winspool. h |
| [**Caps do co-processador \_ \_ 2**](printprocessor-caps-2.md)          | Representa informações de capacidade da impressora.                                             | Winspool. h |



 

As seguintes funções, enumerações e interfaces são usadas para implementar um novo sistema de notificação de impressão assíncrona.



| Função                                                                             | Descrição                                                                                                                                                                                       | Cabeçalho     | Biblioteca      |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)               | Cria um canal de comunicação entre o componente de impressão hospedado no spooler, como um driver de impressão ou monitor de porta, e um aplicativo que precisa receber notificações do componente. | Prnasnot. h | Winspool. lib |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)     | Registra um aplicativo para receber notificações de componentes hospedados no spooler, como drivers de impressora, processadores de impressão e monitores de porta.                                                    | Prnasnot. h | Winspool. lib |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications) | Habilita um aplicativo que se registrou para receber notificações de componentes de impressão hospedados no spooler para encerrar sua assinatura para as notificações.                                         | Prnasnot. h | Winspool. lib |



 



| Enumeração                                                                    | Descrição                                                                                                                                                                                                          | Cabeçalho     |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| [**PrintAsyncNotifyConversationStyle**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle) | Especifica se a comunicação entre aplicativos e os componentes hospedados no spooler de impressão, como drivers de impressora, processadores de impressão e monitores de porta, é bidirecional ou unidirecional.                          | Prnasnot. h |
| [**PrintAsyncNotifyError**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)                         | Especifica um erro em uma transação de notificação assíncrona.                                                                                                                                                      | Prnasnot. h |
| [**PrintAsyncNotifyUserFilter**](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)               | Especifica se as notificações vão apenas para a escuta de aplicativos associados ao mesmo usuário que o remetente hospedado pelo spooler de impressão ou se eles vão para um conjunto mais amplo de aplicativos de escuta. | Prnasnot. h |



 



| Interface e método                                                                                                      | Descrição                                                                                                                                                   | Cabeçalho     | Biblioteca      |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------|
| [**IPrintAsyncNotifyCallback::ChannelClosed**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-channelclosed)    | Usado por um membro de um canal de comunicação para informar ao outro membro que o canal está sendo fechado.                                                    | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyCallback::OnEventNotify**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifycallback-oneventnotify)    | Chamado pelo spooler de impressão para alertar um ouvinte de que uma notificação está disponível em um canal especificado.                                                      | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel::CloseChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-closechannel)         | Fecha um canal de comunicação.                                                                                                                               | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyChannel:: SendNotification**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifychannel-sendnotification) | Envia uma notificação de um componente hospedado pelo spooler de impressão para um ou mais aplicativos de escuta ou envia uma resposta de um aplicativo de volta para um componente. | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::AcquireData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-acquiredata)  | Aponta os aplicativos de escuta para os dados de notificação, bem como o tamanho e o tipo dos dados.                                                                   | Prnasnot. h | Winspool. lib |
| [**IPrintAsyncNotifyDataObject::ReleaseData**](/windows/desktop/api/prnasnot/nf-prnasnot-iprintasyncnotifydataobject-releasedata)  | Libera a memória usada pelos dados encapsulados no [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject).                                  | Prnasnot. h | Winspool. lib |



 

A seguinte enumeração e estruturas são usadas para invocar o conversor de documento XPS da Microsoft (MXDC), que grava documentos XPS (XML Paper Specification) em um dispositivo ou arquivo.



| Enumeração                                | Descrição                                                            | Cabeçalho |
|--------------------------------------------|------------------------------------------------------------------------|--------|
| [**MxdcS0PageEnums**](mxdcs0pageenums.md) | Especifica os tipos de recursos, como fontes ou imagens, em uma página XPS. | Mxdc. h |



 



| Estrutura                                                          | Descrição                                                                                                                                    | Cabeçalho |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| [**MxdcEscapeHeader**](mxdcescapeheader.md)                       | Representa uma instrução para o MXDC.                                                                                                         | Mxdc. h |
| [**MxdcGetFileNameData**](mxdcgetfilenamedata.md)                 | Representa o caminho completo e o nome de um arquivo de saída MXDC.                                                                                     | Mxdc. h |
| [**MxdcPrintTicketEscape**](mxdcprintticketescape.md)             | Representa uma combinação de [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md). | Mxdc. h |
| [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md)   | Representa um tíquete de impressão que será associado a um documento XPS.                                                                        | Mxdc. h |
| [**MxdcS0PageData**](mxdcs0pagedata.md)                           | Representa uma página formatada em XPS a ser passada para o arquivo de saída MXDC sem nenhum processamento.                                                  | Mxdc. h |
| [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) | Representa uma combinação de [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcS0PageData**](mxdcs0pagedata.md).                         | Mxdc. h |
| [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md)       | Representa uma combinação de [**MxdcEscapeHeader**](mxdcescapeheader.md) e [**MxdcS0PageResource**](mxdcs0pageresourceescape.md).           | Mxdc. h |
| [**MxdcS0PageResource**](mxdcs0pageresourceescape.md)             | Representa um recurso, como uma fonte ou imagem, que está incluído em uma página XPS pelo MXDC.                                                   | Mxdc. h |



 

 

 
