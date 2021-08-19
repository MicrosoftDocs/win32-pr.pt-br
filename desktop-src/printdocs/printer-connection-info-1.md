---
description: Representa informações sobre uma conexão com uma impressora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b9adbe18d3f75062a67440fd7f7586c4336323ff3035416f3ad9799f5e34a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033894"
---
# <a name="printer_connection_info_1-structure"></a>Estrutura INFORMAÇÕES \_ DE CONEXÃO DA IMPRESSORA \_ \_ 1

Representa informações sobre uma conexão com uma impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwFlags**
</dt> <dd>

Os seguintes valores são definidos:



| Valor                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INCOMPATIBILIDADE \_ DE CONEXÃO DE IMPRESSORA \_ (0x00000020) | Se esse sinalizador de bit estiver definido, a conexão de impressora será incompatibilidade. O usuário pode fornecer um driver de impressão local como *pszDriverName* e usá-lo para fazer a renderização em vez de usar o driver instalado na impressora do servidor à qual o usuário está conectado.<br/>                                                                                                                                                                                                                                    |
| CONEXÃO \_ DE IMPRESSORA SEM INTERFACE DO USUÁRIO \_ \_ (0x00000040)   | Se esse sinalizador de bit estiver definido, essa chamada não poderá exibir uma caixa de diálogo. Se uma caixa de diálogo tiver que ser exibida para instalar um driver de impressora do servidor e esse sinalizador de bit estiver definido, o driver de impressora não será instalado, a conexão de impressora não será adicionada e a chamada falhará.<br/> **Windows 7:** No Windows 7 e versões posteriores do Windows, se esse sinalizador estiver definido e o usuário estiver em execução no modo elevado, a caixa de diálogo Confiar nessa **impressora?** não será mostrada.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Um ponteiro para o nome do driver.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




