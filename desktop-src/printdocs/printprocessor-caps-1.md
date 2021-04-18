---
description: A estrutura do multiprocessador \_ Caps \_ 1 é o formato para as informações de capacidade da impressora que são retornadas pela função GetPrinterData no buffer especificado pela variável pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Estrutura de PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796103"
---
# <a name="printprocessor_caps_1-structure"></a>Estrutura de Caps-PROCESSer \_ \_ 1

A estrutura do **multiprocessador \_ Caps \_ 1** é o formato para as informações de capacidade da impressora que são retornadas pela função [**GetPrinterData**](getprinterdata.md) no buffer especificado pela variável *pData* .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwLevel**
</dt> <dd>

O número de versão da estrutura. Esse valor deve ser 1.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Uma máscara de bits que representa os vários números de páginas de documentos que a impressora pode imprimir em uma página física. O bit menos significativo representa 1 página de documento por página, o próximo bit representa 2 páginas de documento por página e assim por diante. Por exemplo, 0x0000810B indica que a impressora dá suporte a 1, 2, 4, 9 e 16 páginas de documento por página física.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

A ordem na qual as páginas serão impressas. Esse valor pode ser \_ impressão normal, impressão reversa \_ ou impressão de livretos \_ .

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

O número máximo de cópias que a impressora pode manipular.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores para todos os membros da estrutura são fornecidos pela função [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , que está documentada no WDK (Kit de driver do Windows).

O spooler chama uma função [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) do processador de impressão quando um aplicativo chama [**GetPrinterData**](getprinterdata.md), especificando um nome de valor com um formato de \_ *DataType* PrintProcCaps, em que *DataType* é o nome de um tipo de dados de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

