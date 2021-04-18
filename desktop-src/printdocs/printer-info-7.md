---
description: A \_ estrutura informações da impressora \_ 7 especifica informações sobre a impressora dos serviços de diretório.
ms.assetid: 9443855e-df7d-41a1-a0df-5649a97b2915
title: Estrutura de PRINTER_INFO_7 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_7
- _PRINTER_INFO_7A
- _PRINTER_INFO_7W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3dfa92ead4a1f7dab4f0610145e1e1dee7d04065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793661"
---
# <a name="printer_info_7-structure"></a>Estrutura de informações da impressora \_ \_ 7

A **estrutura \_ informações \_ da impressora 7** especifica informações sobre a impressora dos serviços de diretório. Use essa estrutura com a função [**Setprintr**](setprinter.md) para publicar os dados de uma impressora no serviço de diretório (DS) ou para atualizar ou remover os dados publicados de uma impressora do DS. Use essa estrutura com a função [**Getprinter**](getprinter.md) para determinar se uma impressora é publicada no DS.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_7 {
  LPTSTR pszObjectGUID;
  DWORD  dwAction;
} PRINTER_INFO_7, *PPRINTER_INFO_7;
```



## <a name="members"></a>Membros

<dl> <dt>

**pszObjectGUID**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o GUID do objeto de fila de impressão do serviço de diretório associado a uma impressora publicada. Use a função [**Getprintr**](getprinter.md) para recuperar esse GUID.

Antes de chamar [**Setprinter**](setprinter.md), defina **pszObjectGUID** como **nulo**.

</dd> <dt>

**dwAction**
</dt> <dd>

Indica a ação da função [**Setprinter**](setprinter.md) a ser executada. Para a função [**Getprinter**](getprinter.md) , esse membro indica se a impressora especificada foi publicada. Esse membro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DSPRINT_PENDING"></span><span id="dsprint_pending"></span><dl> <dt>**DSPRINT \_**</dt> <dt>0x80000000</dt> pendente </dl>       | [**Getprinter**](getprinter.md): indica que o sistema está tentando concluir uma operação de publicação ou cancelamento de publicação iniciada por uma chamada [**setprinter**](setprinter.md) .<br/> [**Setprinter**](setprinter.md): esse valor não é válido. <br/>                                                |
| <span id="DSPRINT_PUBLISH"></span><span id="dsprint_publish"></span><dl> <dt>**DSPRINT \_ PUBLICAR**</dt> <dt>0x00000001</dt> </dl>       | [**Setprinter**](setprinter.md): publica os dados da impressora no DS.<br/> [**Getprinter**](getprinter.md): indica que a impressora foi publicada. <br/>                                                                                                                                      |
| <span id="DSPRINT_REPUBLISH"></span><span id="dsprint_republish"></span><dl> <dt>**DSPRINT \_ Republicar**</dt> <dt>0x00000008</dt> </dl> | [**Setprinter**](setprinter.md): os dados DS da impressora não são publicados e, em seguida, publicados novamente, atualizando todas as propriedades na impressora publicada. A nova publicação também altera o GUID da impressora publicada.<br/> [**Getprinter**](getprinter.md): nunca retorna esse valor. <br/> |
| <span id="DSPRINT_UNPUBLISH"></span><span id="dsprint_unpublish"></span><dl> <dt>**DSPRINT \_ Cancelar publicação**</dt> de <dt>0x00000004</dt> </dl> | [**Setprinter**](setprinter.md): remove os dados publicados da impressora do DS.<br/> [**Getprinter**](getprinter.md): indica que a impressora não está publicada. <br/>                                                                                                                        |
| <span id="DSPRINT_UPDATE"></span><span id="dsprint_update"></span><dl> <dt>**DSPRINT \_ ATUALIZAÇÃO**</dt> <dt>0x00000002</dt> </dl>          | [**Setprinter**](setprinter.md): atualiza os dados publicados da impressora no DS.<br/> [**Getprinter**](getprinter.md): nunca retorna esse valor. <br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **informações da impressora \_ \_ 7** é usada em uma chamada de [**reimpressões**](setprinter.md) para publicar informações da impressora no serviço de diretório. Os dados publicados incluem todos os valores e dados da impressora especificada encontrados na chave do \_ spooler SPLDS \_ , chave de \_ Driver SPLDS \_ ou chaves de \_ chave de usuário SPLDS \_ criadas [**por SetPrinterDataEx**](setprinterdataex.md).

Para [**Setprinter**](setprinter.md), *pszObjectGUID* deve ser definido como **NULL**. Para [**Getprinter**](getprinter.md), *PSZOBJECTGUID* retorna o GUID do objeto de fila de impressão dos serviços de diretório associado a uma impressora publicada. Você pode usar esse GUID com métodos de interface de serviços de Active Directory (ADSI) para recuperar dados publicados para a impressora. No entanto, o método recomendado para recuperar dados publicados é chamar a função [**GetPrinterDataEx**](getprinterdataex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 7W** (Unicode) e **\_ informações de impressora \_ \_ 7a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




