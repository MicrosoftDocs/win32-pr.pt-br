---
description: Especifica o cache de um alça para uma impressora aberta com OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: PRINTER_OPTION_FLAGS enumeração (Winspool.h)
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
ms.openlocfilehash: b8541ec00f0d53bf58a826ceb7d8b8a821008fb6a66c0fe3917ebc12822e0e5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091796"
---
# <a name="printer_option_flags-enumeration"></a>\_Enumeração PRINTER OPTION \_ FLAGS

Especifica o cache de um alça para uma impressora aberta com [**OpenPrinter2.**](openprinter2.md)

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

<span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**OPÇÃO \_ IMPRESSORA \_ SEM \_ CACHE**
</dt> <dd>

O handle não é armazenado em cache. Todas as funções aplicadas a um handle retornado pelo [**OpenPrinter2**](openprinter2.md) serão para o computador remoto.

</dd> <dt>

<span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**CACHE DE \_ OPÇÕES DA \_ IMPRESSORA**
</dt> <dd>

O handle é armazenado em cache. Todas as funções aplicadas a um handle retornado por [**OpenPrinter2**](openprinter2.md) serão para o cache local.

</dd> <dt>

<span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**ALTERAÇÃO DO CLIENTE DA OPÇÃO IMPRESSORA \_ \_ \_**
</dt> <dd>

O handle retornado pelo [**OpenPrinter2**](openprinter2.md) pode ser usado pelo [**SetPrinter**](setprinter.md) para renomear a conexão de impressora.

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
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




