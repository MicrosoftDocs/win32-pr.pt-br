---
description: A estrutura DRIVER \_ INFO \_ 3 contém informações de driver de impressora.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: DRIVER_INFO_3 (Winspool.h)
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
ms.openlocfilehash: 8187b90ee9cc423051b8b57d942fa026cca6f8c3d3bbfabd7721ed204484cb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234908"
---
# <a name="driver_info_3-structure"></a>Estrutura INFORMAÇÕES \_ \_ DO DRIVER 3

A **estrutura DRIVER INFO \_ \_ 3** contém informações de driver de impressora.

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

A versão do sistema operacional para a qual o driver foi gravado. Os valores com suporte são 3 e 4, que representam os drivers V3 e V4, respectivamente.

</dd> <dt>

**Pname**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi gravado (por exemplo, Windows x86, Windows IA64 e Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, "C: \\ DRIVERS \\Pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém dados de driver (por exemplo, "C: \\ DRIVERS \\ Qms810.ppd").

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

Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo. Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo de que o driver depende. A sequência de cadeias de caracteres é encerrada por uma cadeia de caracteres vazia de comprimento zero. Se **pDependentFiles** não for **NULL** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de linguagem (por exemplo, "Monitor PJL"). Esse membro pode ser **NULL** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.

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
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DO DRIVER \_ 3W** (Unicode) e **\_ INFORMAÇÕES DO DRIVER \_ \_ 3A** (ANSI)<br/>                             |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




