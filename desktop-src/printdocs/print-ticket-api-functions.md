---
description: As funções a seguir são usadas para gerenciar tíquetes de impressão.
ms.assetid: 9e942a1d-660b-4691-9282-ffb49e0b9848
title: Funções da API de tíquete de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5dfda941d0b0f7d99b0ffbef703a98e357ccc6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828918"
---
# <a name="print-ticket-api-functions"></a>Funções da API de tíquete de impressão

As funções a seguir são usadas para gerenciar tíquetes de impressão.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                                  | Descrição                                                                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertDevModeToPrintTicketThunk2**](convertdevmodetoprintticketthunk2.md)<br/> | Converte uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) em um tíquete de impressão.<br/>                                                                          |
| [**ConvertPrintTicketToDevModeThunk2**](convertprinttickettodevmodethunk2.md)<br/> | Converte um tíquete de impressão em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                          |
| [**MergeAndValidatePrintTicketThunk2**](mergeandvalidateprintticketthunk2.md)<br/> | Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.<br/>                                                                          |
| [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)<br/>                                     | Fecha um identificador de provedor de tíquete de impressão.<br/>                                                                                                      |
| [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)<br/>         | Converte uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) em um tíquete de impressão dentro de um [**IStream**](/windows/desktop/Stg/istream-compound-file-implementation).<br/>        |
| [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)<br/>         | Converte um tíquete de impressão em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .<br/>                                                                        |
| [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)<br/>                       | Recupera os recursos da impressora formatados em conformidade com o [esquema de impressão](./printschema.md)XML.<br/>                   |
| [**PTGetPrintDeviceCapabilities**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities)<br/>    | Recupera os recursos da impressora do dispositivo formatados em conformidade com o [esquema de impressão](./printschema.md)XML.<br/>            |
| [**PTGetPrintDeviceResources**](/windows/win32/api/prntvpt/nf-prntvpt-ptgetprintdeviceresources)<br/>          | Ele recupera os recursos dos dispositivos de impressão para uma impressora formatada em conformidade com o [esquema de impressão](./printschema.md)XML.<br/> |
| [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)<br/>         | Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.<br/>                                                                          |
| [**PTOpenProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider)<br/>                                       | Abre uma instância de um provedor de tíquete de impressão.<br/>                                                                                               |
| [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)<br/>                                   | Abre uma instância de um provedor de tíquete de impressão.<br/>                                                                                               |
| [**PTQuerySchemaVersionSupport**](/windows/desktop/api/prntvpt/nf-prntvpt-ptqueryschemaversionsupport)<br/>             | Recupera a versão mais alta (mais recente) do [esquema de impressão](./printschema.md) compatível com a impressora especificada.<br/>           |
| [**PTReleaseMemory**](/windows/desktop/api/prntvpt/nf-prntvpt-ptreleasememory)<br/>                                     | Libera buffers associados a recursos de impressão e Tíquetes de impressão.<br/>                                                                      |
| [**UnbindPTProviderThunk**](unbindptproviderthunk.md)<br/>                         | Fecha um identificador para um provedor de tíquete de impressão.<br/>                                                                                                 |



 

 

