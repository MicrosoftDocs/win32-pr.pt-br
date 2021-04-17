---
description: A \_ estrutura informações do driver \_ 3 contém informações de driver de impressora.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Estrutura de DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791432"
---
# <a name="driver_info_3-structure"></a>Estrutura de informações do DRIVER \_ \_ 3

A **estrutura \_ informações \_ do Driver 3** contém informações de driver de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DRIVER_INFO_3 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a>Membros

<dl> <dt>

**cVersion**
</dt> <dd>

A versão do sistema operacional para a qual o driver foi gravado. Os valores com suporte são 3 e 4, que representam os drivers v3 e v4, respectivamente.

</dd> <dt>

**pName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, "C: \\ DRIVERS \\Pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, "C: \\ drivers \\ Qms810. PPD").

</dd> <dt>

**pConfigFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, "C: \\ DRIVERS \\Pscrptui.dll").

</dd> <dt>

**pHelpFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo.

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

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ Driver \_ \_ 3W** (Unicode) e **\_ info de driver \_ \_ 3a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




