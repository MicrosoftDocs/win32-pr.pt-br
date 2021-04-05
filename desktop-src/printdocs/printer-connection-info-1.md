---
description: Representa informações sobre uma conexão a uma impressora.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: Estrutura de PRINTER_CONNECTION_INFO_1 (winspool. h)
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
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662449"
---
# <a name="printer_connection_info_1-structure"></a>Estrutura de informações de conexão da impressora \_ \_ \_ 1

Representa informações sobre uma conexão a uma impressora.

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
| \_Incompatibilidade \_ de conexão de impressora (0x00000020) | Se esse sinalizador de bit estiver definido, a conexão de impressora não corresponde. O usuário pode fornecer um driver de impressão local como *pszDriverName* e usá-lo para fazer a renderização em vez de usar o driver instalado na impressora do servidor à qual o usuário está conectado.<br/>                                                                                                                                                                                                                                    |
| \_Conexão \_ de impressora sem \_ interface do usuário (0x00000040)   | Se esse sinalizador de bit estiver definido, essa chamada não poderá exibir uma caixa de diálogo. Se for necessário exibir uma caixa de diálogo para instalar um driver de impressora a partir do servidor e esse sinalizador de bits estiver definido, o driver de impressora não será adicionado e a chamada falhará.<br/> **Windows 7:** No Windows 7 e versões posteriores do Windows, se esse sinalizador estiver definido e o usuário estiver sendo executado no modo elevado, a caixa de diálogo **você confia nesta impressora?** não será exibida.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Um ponteiro para o nome do driver.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




