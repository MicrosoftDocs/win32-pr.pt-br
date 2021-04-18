---
description: A \_ estrutura informações sobre o driver \_ 6 contém informações de driver de impressora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Estrutura de DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807266"
---
# <a name="driver_info_6-structure"></a>Estrutura de informações do DRIVER \_ \_ 6

A **estrutura \_ informações \_ sobre o driver 6** contém informações de driver de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a>Membros

<dl> <dt>

**cVersion**
</dt> <dd>

A versão do sistema operacional para a qual o driver foi gravado. O valor com suporte é 3.

</dd> <dt>

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows NT x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ drivers \\ pscrptui. hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo. Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende. A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero. Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, "Monitor de PJL"). Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores que são compatíveis com este driver. Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

A data do pacote de driver, conforme codificado nos arquivos de driver.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Número de versão do driver. Isso sai da estrutura de versão do driver.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do fabricante.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL para o fabricante.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica a ID de hardware para o driver de impressora.

</dd> <dt>

**pszProvider**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o provedor do driver de impressora (por exemplo, "Microsoft Windows 2000")

</dd> </dl>

## <a name="remarks"></a>Comentários

As cadeias de caracteres para esses membros estão contidas no arquivo. inf que é usado para adicionar o driver.

Se você chamar [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md) com *nível* diferente de 6 e, em seguida, chamar [**GetPrinterDriver**](getprinterdriver.md) ou [**EnumPrinterDrivers**](enumprinterdrivers.md) com o *nível* igual a 6, a estrutura **informações do driver \_ \_ 6** será retornada com **pszMfgName**, **pszOEMUrl**, **pszHardwareID** e **pszProvider** definida como **NULL**, **dwlDriverVersion** definida como 0 e **ftDriverDate** definida como (0, 0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações do **\_ Driver \_ \_ 6W** (Unicode) e **\_ info do driver \_ \_ 6a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




