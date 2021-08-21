---
title: XTYP_MONITOR transações (Ddeml.h)
description: Uma função de retorno de chamada DDE (Dados Dinâmicos Exchange) do depurador DDE, DdeCallback, recebe a transação XTYP MONITOR sempre que um evento DDE ocorre \_ no sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a86235c2964bbd09d51ce3adc2e602e23fed09597df14721e92e76c0cd8109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047254"
---
# <a name="xtyp_monitor-transaction"></a>Transação do MONITOR \_ XTYP

Uma função de retorno de chamada DDE (Dados Dinâmicos Exchange) do depurador DDE, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação **XTYP \_ MONITOR** sempre que um evento DDE ocorre no sistema. Para receber essa transação, um aplicativo deve especificar o **valor APPCLASS \_ MONITOR** quando chama a [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

Não usado.

</dd> <dt>

*hconv* 
</dt> <dd>

Não usado.

</dd> <dt>

*hsz1* 
</dt> <dd>

Não usado.

</dd> <dt>

*hsz2* 
</dt> <dd>

Não usado.

</dd> <dt>

*hdata* 
</dt> <dd>

Um identificador para um objeto DDE que contém informações sobre o evento DDE. O aplicativo deve usar a [**função DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obter um ponteiro para o objeto .

</dd> <dt>

*dwData1* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData2* 
</dt> <dd>

O evento DDE. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ RETORNOS DE**</dt> <dt>CHAMADA 0x08000000</dt> </dl> | O sistema enviou uma transação para uma função de retorno de chamada DDE. O objeto DDE contém uma [**estrutura MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) que fornece informações sobre a transação.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_ CONV**</dt> <dt>0x40000000</dt> </dl>                | Uma conversa de DDE foi estabelecida ou encerrada. O objeto DDE contém uma [**estrutura MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) que fornece informações sobre a conversa.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ ERROS**</dt> <dt>0x10000000</dt> </dl>          | Ocorreu um erro de DDE. O objeto DDE contém uma [**estrutura MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) que fornece informações sobre o erro.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ INFO**</dt> <dt>0x01000000</dt> </dl>   | Um aplicativo DDE criado, liberado ou incrementado a contagem de uso de um alça de cadeia de caracteres ou um alça de cadeia de caracteres foi liberado como resultado de uma chamada para a [**função DdeUninitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) O objeto DDE contém uma [**estrutura MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) que fornece informações sobre o identificador de cadeia de caracteres.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ LINKS**</dt> <dt>0x20000000</dt> </dl>             | Um aplicativo DDE iniciou ou interrompeu um loop de consultoria. O objeto DDE contém uma [**estrutura MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) que fornece informações sobre o loop de consultoria.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ POSTMSGS**</dt> <dt>0x04000000</dt> </dl>    | O sistema ou um aplicativo postou uma mensagem DDE. O objeto DDE contém uma [**estrutura MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ SendMSGS**</dt> <dt>0x02000000</dt> </dl>    | O sistema ou um aplicativo enviou uma mensagem DDE. O objeto DDE contém uma [**estrutura MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função de retorno de chamada processa essa transação, ela deve retornar 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

