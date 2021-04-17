---
description: Especifica as funções de retorno de chamada a serem usadas pelo Gerenciador de componentes opcional.
ms.assetid: 454cc07e-4a00-4c53-9759-47563a8ed62f
title: Estrutura de OCM_CLIENT_CALLBACKS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OCM_CLIENT_CALLBACKS
api_type:
- NA
api_location: ''
ms.openlocfilehash: cc2c1d95e2b05de1ad7285e065e9742a24e0e5a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754908"
---
# <a name="ocm_client_callbacks-structure"></a>\_Estrutura de \_ retornos de chamada do cliente OCM

Especifica as funções de retorno de chamada a serem usadas pelo Gerenciador de componentes opcional.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _OCM_CLIENT_CALLBACKS {
  POC_FILL_IN_SETUP_DATA_PROC_A     FillInSetupDataA;
  POC_LOG_ERROR                     LogError;
  POC_SET_REBOOT_PROC               SetReboot;
  POC_SHOWHIDEWIZARDPAGE            ShowHideWizardPage;
  POC_BILLBOARD_PROGRESS_CALLBACK   BillboardProgressCallback;
  POC_BILLBOARD_SET_PROGRESS_TEXT_A BillBoardSetProgressText;
  POC_SETUP_PERF_DATA               SetupPerfData;
} OCM_CLIENT_CALLBACKS, *POCM_CLIENT_CALLBACKS;
```



## <a name="members"></a>Membros

<dl> <dt>

**FillInSetupDataA**
</dt> <dd>

A função de retorno de chamada para preencher a estrutura de dados de instalação que fornece informações sobre o ambiente no qual o Gerenciador de OC está em execução.

</dd> <dt>

**LogError**
</dt> <dd>

A função de retorno de chamada que registra quaisquer erros.

</dd> <dt>

**Reboot**
</dt> <dd>

A função de retorno de chamada que indica a necessidade de reinicializar.

</dd> <dt>

**ShowHideWizardPage**
</dt> <dd>

A função de retorno de chamada que indica se o assistente deve ser mostrado ou ocultado. Isso só terá efeito se o mural for mostrado.

</dd> <dt>

**BillboardProgressCallback**
</dt> <dd>

A função de retorno de chamada que chama os comentários de progresso para o mural.

</dd> <dt>

**BillBoardSetProgressText**
</dt> <dd>

A função de retorno de chamada que especifica a cadeia de caracteres a ser exibida na barra de progresso.

</dd> <dt>

**SetupPerfData**
</dt> <dd>

A função de retorno de chamada que define os dados de desempenho.

</dd> </dl>

## <a name="remarks"></a>Comentários

As funções de retorno de chamada são declaradas da seguinte maneira.

``` syntax
typedef
VOID
(WINAPI *POC_FILL_IN_SETUP_DATA_PROC_A)(
    OUT PSETUP_DATAA SetupData
    );
typedef
VOID
(WINAPI *POC_FILL_IN_SETUP_DATA_PROC_W)(
    OUT PSETUP_DATAW SetupData
    );

typedef struct _SETUP_DATAA {
    DWORD SetupMode;
    DWORD ProductType;
    DWORDLONG OperationFlags;
    CHAR SourcePath[MAX_PATH];
    CHAR UnattendFile[MAX_PATH];
} SETUP_DATAA, *PSETUP_DATAA;

typedef struct _SETUP_DATAW {
    DWORD SetupMode;
    DWORD ProductType;
    DWORDLONG OperationFlags;
    WCHAR SourcePath[MAX_PATH];
    WCHAR UnattendFile[MAX_PATH];
} SETUP_DATAW, *PSETUP_DATAW;

#ifdef UNICODE
typedef SETUP_DATAW SETUP_DATA;
typedef PSETUP_DATAW PSETUP_DATA;
#else
typedef SETUP_DATAA SETUP_DATA;
typedef PSETUP_DATAA PSETUP_DATA;
#endif

#define SETUPMODE_UNKNOWN       (-1)
#define SETUPMODE_MINIMAL       0
#define SETUPMODE_TYPICAL       1
#define SETUPMODE_LAPTOP        2
#define SETUPMODE_CUSTOM        3

#define SETUPMODE_PRIVATE(x)    ((x) & SETUPMODE_PRIVATE_MASK)

#define SETUPMODE_UPGRADEONLY   0x20000100
#define SETUPMODE_ADDEXTRACOMPS 0x20000200

#define SETUPMODE_ADDREMOVE     0x10000100
#define SETUPMODE_REINSTALL     0x10000200
#define SETUPMODE_REMOVEALL     0x10000400

#define SETUPMODE_FRESH         0x00000000
#define SETUPMODE_MAINTENANCE   0x10000000
#define SETUPMODE_UPGRADE       0x20000000

#define PRODUCT_WORKSTATION         0
#define PRODUCT_SERVER_PRIMARY      1
#define PRODUCT_SERVER_STANDALONE   2
#define PRODUCT_SERVER_SECONDARY    3

#define SETUPOP_WIN31UPGRADE        0x0000000000000001
#define SETUPOP_WIN95UPGRADE        0x0000000000000002
#define SETUPOP_NTUPGRADE           0x0000000000000004
#define SETUPOP_BATCH               0x0000000000000008
#define SETUPOP_STANDALONE          0x0000000000000010
#define SETUPOP_AMD64_FILES_AVAIL   0x0000000100000000
#define SETUPOP_OBSOLETE1_FILES_AVAIL 0x0000000200000000 
#define SETUPOP_OBSOLETE2_FILES_AVAIL 0x0000000400000000
#define SETUPOP_X86_FILES_AVAIL     0x0000000800000000
#define SETUPOP_IA64_FILES_AVAIL    0x0000001000000000
```

``` syntax
typedef
INT
(WINAPIV *POC_LOG_ERROR)(
    IN OcErrorLevel Level,
    IN LPCTSTR      FormatString,
    ...
    );

typedef enum {
    OcErrLevInfo    = 0x00000000,
    OcErrLevWarning = 0x01000000,
    OcErrLevError   = 0x02000000,
    OcErrLevFatal   = 0x03000000,
    OcErrLevMax     = 0x04000000,
    OcErrBatch      = 0x10000000,
    OcErrMask           = 0xFF000000
} OcErrorLevel;
```

``` syntax
typedef
VOID
(WINAPI *POC_SET_REBOOT_PROC)(
    VOID
    );
```

``` syntax
typedef
HWND 
(WINAPI *POC_SHOWHIDEWIZARDPAGE)(
    IN BOOL bShow
    );
```

``` syntax
typedef
LRESULT
(WINAPI *POC_BILLBOARD_PROGRESS_CALLBACK)(
    IN UINT     Msg,
    IN WPARAM   wParam,
    IN LPARAM   lParam
    );
```

``` syntax
typedef 
VOID
(WINAPI *POC_BILLBOARD_SET_PROGRESS_TEXT_W)(
    IN PWSTR Text
    );

typedef 
VOID
(WINAPI *POC_BILLBOARD_SET_PROGRESS_TEXT_A)(
    IN PSTR Text
    );
```

``` syntax
typedef 
VOID
(WINAPI *POC_SETUP_PERF_DATA)(
    IN PWSTR FileName,
    IN ULONG LineNumber,
    IN PWSTR TagStr,
    IN PWSTR FormatStr,
    ...
    );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 



