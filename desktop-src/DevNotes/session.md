---
description: A estrutura de sessão contém informações sobre a sessão atual.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Estrutura de sessão
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646192"
---
# <a name="session-structure"></a>Estrutura de sessão

\[Esta estrutura contém informações necessárias apenas ao usar as funções **DeleteExtractedFiles** e **Extract** , que não têm suporte. Esta documentação é fornecida apenas para fins informativos.\]

A estrutura de **sessão** contém informações sobre a sessão atual.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Act**
</dt> <dd>

a ação a ser executada. Esse membro pode ser um dos valores do seguinte tipo enumerado.

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

**hflist**
</dt> <dd>

O identificador para uma lista de arquivos especificados na linha de comando. Esse tipo de dados é declarado da seguinte maneira:

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

Um sinalizador que indica se mais de um arquivo de gabinete deve ser processado. Se esse valor for **true**, os gabinetes de continuação serão processados.

</dd> <dt>

**fOverwrite**
</dt> <dd>

Um sinalizador que indica se os arquivos existentes devem ser substituídos. Se esse valor for **true**, os arquivos existentes serão substituídos.

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

Um sinalizador que indica se a última `printf` chamada tem os caracteres de nova linha ( `\n` ). Se esse valor for **true**, a última `printf` chamada não incluirá os caracteres de nova linha.

</dd> <dt>

**fSelfExtract**
</dt> <dd>

Um sinalizador que indica se um gabinete está auto-extraível. Se esse valor for **true**, o gabinete será auto-extraível.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

O comprimento da parte executável (. exe) de um gabinete de extração automática.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

O comprimento da parte do CAB de um gabinete de extração automática.

</dd> <dt>

**ahfSelf**
</dt> <dd>

Os identificadores de arquivo para o gabinete.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

A contagem de erros encontrados durante a sessão de extração.

</dd> <dt>

**hfdi**
</dt> <dd>

Um identificador para o contexto FDI. Esse tipo de dados é declarado da seguinte maneira:

`typedef void FAR *HFDI; `

</dd> <dt>

**erf**
</dt> <dd>

A estrutura de erro FDI. Consulte [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**recfiles**
</dt> <dd>

A contagem de arquivos processados.

</dd> <dt>

**cbTotalBytes**
</dt> <dd>

O número total de bytes extraídos.

</dd> <dt>

**perr**
</dt> <dd>

O FDI de passagem.

</dd> <dt>

**Java**
</dt> <dd>

O erro do arquivo de despejo. Esse membro pode ser um dos valores do seguinte tipo enumerado.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbSpill**
</dt> <dd>

O tamanho do arquivo de despejo solicitado.

</dd> <dt>

**achSelf**
</dt> <dd>

O nome do arquivo executável (. exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

O buffer de formatação de mensagens.

`#define cbMAX_LINE          256`

</dd> <dt>

**achLine**
</dt> <dd>

O buffer de formatação de linha.

</dd> <dt>

**achLocation**
</dt> <dd>

O diretório de saída.

</dd> <dt>

**achFile**
</dt> <dd>

O nome de arquivo atual que está sendo extraído.

</dd> <dt>

**achDest**
</dt> <dd>

O nome do arquivo de destino forçado.

</dd> <dt>

**achCabPath**
</dt> <dd>

O caminho para examinar um arquivo de gabinete.

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

Um sinalizador que indica se o gabinete atual é o primeiro processado. Se definido como **true**, ele não é o primeiro gabinete processado.

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

Um sinalizador que indica se as informações de reserva devem ser fornecidas. Se definido como **true**, as informações serão disponibilizadas.

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

Esse membro fornece uma maneira de determinar qual das entradas **acab** usar se estiver processando todos os arquivos em um conjunto de gabinetes (**fAllCabinet** é definido como **true**).

</dd> <dt>

**acab**
</dt> <dd>

As duas últimas entradas no conjunto de gabinetes. Essa estrutura é definida da seguinte maneira:

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

**achZap**
</dt> <dd>

O prefixo a ser tirado do nome do arquivo.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

O arquivo de gabinete atual.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

O argc de extração automática padrão.

</dd> <dt>

**pArgv**
</dt> <dd>

Um ponteiro para um ponteiro para o argv de extração automática padrão \[ \] .

</dd> <dt>

**fDestructive**
</dt> <dd>

Um sinalizador que minimiza o espaço em disco necessário quando definido como **true**.

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

Se **fDestructive** for definido como **true**, extraia apenas a pasta atual.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Extração**](extract.md)
</dt> </dl>

 

 
