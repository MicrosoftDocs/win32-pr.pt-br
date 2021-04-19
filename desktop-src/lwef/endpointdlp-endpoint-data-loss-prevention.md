---
description: As APIs de DLP (prevenção de perda de dados) do ponto de extremidade permitem que os aplicativos notifiquem o sistema operacional antes e depois de determinadas operações, como abrir ou salvar um arquivo.
title: Prevenção de perda de dados do ponto de extremidade
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 3b8576f9eadd0037eca56c0ba183ea1d1825679a
ms.sourcegitcommit: 8b543a86e551cb5b4270a3cc3590ad0758fb6156
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2021
ms.locfileid: "107526086"
---
# <a name="endpoint-data-loss-prevention"></a>Prevenção de perda de dados do ponto de extremidade

O Windows 10 implementa mecanismos que ajudam a evitar a perda de dados para arquivos confidenciais. As APIs de DLP (prevenção de perda de dados) do ponto de extremidade permitem que os aplicativos notifiquem o sistema operacional antes e depois de determinadas operações, como abrir ou salvar um arquivo. Essas notificações servem como "dicas" que permitem que o sistema Otimize as operações de perda de dados.

## <a name="location-of-the-dlp-dll"></a>Local da dll DLP

Como a DLL do Endpoint DLP não é empacotada com o SDK do Windows, os aplicativos precisarão carregar a dll manualmente no tempo de execução. O caminho para o local da dll é armazenado no registro. A tabela a seguir lista as chaves e os valores do registro que armazenam essas informações. Esses caminhos são definidos como constantes na listagem de código de exemplo endpointdlp. h fornecida abaixo como uma conveniência para os desenvolvedores.

| Constante | Valor | Descrição   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | "EndpointDlp.dll" | O nome da DLL de DLP do ponto de extremidade que fornece a API |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | "SOFTWARE \\ Microsoft \\ Windows Defender" | Chave do registro do Windows Defender em HKLM, em que algumas configurações de DLP de ponto de extremidade são armazenadas |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Valor de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  O caminho do registro na chave HKLM da qual o local de instalação do EndpointDlp.dll pode ser obtido |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | InstallLocation | O valor do registro em ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY no qual o local de instalação do EndpointDlp.dll está armazenado |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | x86 | Em plataformas x64, concatene esse diretório para obter a versão x86 do EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Verificar se o Endpoint DLP está habilitado

Para determinar se o Endpoint DLP está habilitado no sistema, verifique o seguinte valor de chave do registro. 

| Constante | Valor | Descrição   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  " \\ Recursos" | O caminho para a chave de sinalizador habilitada para DLP de ponto de extremidade em (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "SenseDlpEnabled" | O valor do registro em ENDPOINTDLP_ENABLED_FLAG_REGKEY que contém a chave do registro de sinalizador habilitado para DLP

## <a name="endpoint-dlp-apis"></a>APIs DLP de ponto de extremidade

As tabelas a seguir listam as APIs fornecidas pela DLL do Endpoint DLP.

### <a name="initialization-and-versioning"></a>Inicialização e controle de versão

| API | Descrição |
|-----|-------------|
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica o sistema sobre os modos de imposição desejados para um conjunto de operações de DLP (prevenção de perda de dados) de ponto de extremidade.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera a versão da API DLP (prevenção de perda de dados) do ponto de extremidade no dispositivo atual.                                  |


### <a name="document-operations"></a>Operações de documento

| API | Descrição |
|-----|-------------|
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md) | Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada. |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md) | Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.  |
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.                                  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fornece ao sistema informações sobre um documento antes que a operação de abertura seja iniciada.  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação de abertura.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fornece ao sistema informações sobre um documento antes da operação de fechamento do documento ser iniciada.                                  |

### <a name="save-as-operations"></a>Salvar como operações
| API | Descrição |
|-----|-------------|
| [DlpNotifyPreSaveAsDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fornece ao sistema informações sobre um documento antes de uma operação salvar como ser iniciada.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fornece ao sistema informações sobre um documento após a conclusão da operação salvar como.                                  |


### <a name="drag-and-drop-operations"></a>Operações de arrastar e soltar

| API | Descrição |
|-----|-------------|
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é inserido.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fornece ao sistema informações sobre um documento quando um destino de soltar é encerrado.                                  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação arrastar e soltar ser iniciada.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.  |


### <a name="clipboard-operations"></a>opções de Área de Transferência

| API | Descrição |
|-----|-------------|
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação de cópia para a área de transferência ser iniciada.  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação colar da área de transferência ser iniciada.  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação colar da área de transferência.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.                                  |

### <a name="print-operations"></a>Operações de impressão

| API | Descrição |
|-----|-------------|
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fornece ao sistema informações sobre um documento após o início de uma operação de impressão.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.                                  |

## <a name="endpoint-dlp-example-header"></a>Cabeçalho de exemplo do Endpoint DLP

Como o cabeçalho de DLP do ponto de extremidade não está incluído no SDK do Windows, você deve criar o arquivo de cabeçalho por conta própria para obter assinaturas de API para usar em sua implementação. Para sua conveniência, estamos fornecendo um código de exemplo que você pode copiar e colar em seu aplicativo. Além das declarações de função, essa listagem de código também define constantes úteis, como informações de controle de versão e caminhos de chave do registro.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


