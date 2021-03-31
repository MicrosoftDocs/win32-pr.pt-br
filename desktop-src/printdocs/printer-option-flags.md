---
description: Especifica o cache de um identificador para uma impressora aberta com OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Enumeração de PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171026"
---
# <a name="printer_option_flags-enumeration"></a>Enumeração de sinalizadores de \_ opção de impressora \_

Especifica o cache de um identificador para uma impressora aberta com [**OpenPrinter2**](openprinter2.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**opção de impressora \_ \_ sem \_ cache**
</dt> <dd>

O identificador não está armazenado em cache. Todas as funções aplicadas a um identificador retornado pelo [**OpenPrinter2**](openprinter2.md) vão para o computador remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache de opção de impressora \_**
</dt> <dd>

O identificador é armazenado em cache. Todas as funções aplicadas a um identificador retornado por [**OpenPrinter2**](openprinter2.md) vão para o cache local.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**opção da impressora \_ \_ alteração do cliente \_**
</dt> <dd>

O identificador retornado por [**OpenPrinter2**](openprinter2.md) pode ser usado pelo [**setprinter**](setprinter.md) para renomear a conexão de impressora.

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
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

 




