---
description: A \_ estrutura informações sobre o driver \_ 2 identifica um driver de impressora, o número de versão do driver, o ambiente para o qual o driver foi gravado, o nome do arquivo no qual o driver está armazenado e assim por diante.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Estrutura de DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dcb65f066286b5f5cd2fec935fb2223c25cf87fcc64d17de274b9b182a372440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732854"
---
# <a name="driver_info_2-structure"></a>\_Estrutura informações do driver \_ 2

A **estrutura \_ informações \_ sobre o driver 2** identifica um driver de impressora, o número de versão do driver, o ambiente para o qual o driver foi gravado, o nome do arquivo no qual o driver está armazenado e assim por diante.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**cVersion**
</dt> <dd>

A versão do sistema operacional para a qual o driver foi gravado. O valor com suporte é 3.

</dd> <dt>

**pName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi gravado (por exemplo, Windows x86, Windows IA64 e Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Um ponteiro para cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, "c: \\ drivers \\pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, "c: \\ drivers \\ Qms810. PPD").

</dd> <dt>

**pConfigFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a configuração do driver de dispositivo .dll (por exemplo, "c: \\ drivers \\Pscrptui.dll").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de driver **\_ \_ \_ 2W** (Unicode) e **\_ informações de driver \_ \_ 2a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




