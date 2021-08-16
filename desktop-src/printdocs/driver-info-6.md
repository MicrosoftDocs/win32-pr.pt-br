---
description: A estrutura DRIVER \_ INFO \_ 6 contém informações de driver de impressora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: DRIVER_INFO_6 (Winspool.h)
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
ms.openlocfilehash: fd90794fe4c6f41f8704cb626ddfcf9487c89da01afb8a2f8b1fddfe0efea43a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092066"
---
# <a name="driver_info_6-structure"></a>Estrutura \_ INFORMAÇÕES DO DRIVER \_ 6

A **estrutura DRIVER INFO \_ \_ 6** contém informações de driver de impressora.

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

**Pname**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi gravado (por exemplo, Windows NT x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém dados de driver (por exemplo, C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo. Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo de que o driver depende. A sequência de cadeias de caracteres é encerrada por uma cadeia de caracteres vazia de comprimento zero. Se **pDependentFiles** não for **NULL** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de linguagem (por exemplo, "Monitor PJL"). Esse membro pode ser **NULL** e deve ser especificado somente para impressoras capazes de comunicação bidirecional.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores compatíveis com esse driver. Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

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

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL do fabricante.

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

As cadeias de caracteres para esses membros estão contidas no arquivo .inf usado para adicionar o driver.

Se você chamar  [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md) com *Nível* diferente de 6, e, em seguida, você chama [**GetPrinterDriver**](getprinterdriver.md) ou [**EnumPrinterDrivers**](enumprinterdrivers.md) com Nível igual a **\_ \_ 6,** a estrutura DRIVER INFO 6 é retornada com **pszMfgName**, **pszOEMUrl**, **pszHardwareID** e **pszProvider** definido como **NULL,** **dwlDriverVersion** definido como 0 e **ftDriverDate** definido como (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DO DRIVER \_ 6W** (Unicode) e **\_ INFORMAÇÕES DO DRIVER \_ \_ 6A** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




