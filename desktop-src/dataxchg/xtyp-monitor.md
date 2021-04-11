---
title: Transação de XTYP_MONITOR (ddeml. h)
description: Uma função de retorno de chamada DDE do depurador troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação do monitor XTYP sempre que um evento DDE ocorre no sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Troca de dados de transação XTYP_MONITOR
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
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369504"
---
# <a name="xtyp_monitor-transaction"></a>Transação do monitor de XTYP \_

Uma função de retorno de chamada DDE do depurador troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação do **\_ Monitor XTYP** sempre que um evento DDE ocorre no sistema. Para receber essa transação, um aplicativo deve especificar o valor do **\_ Monitor APPCLASS** ao chamar a função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
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

Um identificador para um objeto DDE que contém informações sobre o evento DDE. O aplicativo deve usar a função [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obter um ponteiro para o objeto.

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
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ RETORNOs de chamada**</dt> <dt>0x08000000</dt> </dl> | O sistema enviou uma transação para uma função de retorno de chamada DDE. O objeto DDE contém uma estrutura [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) que fornece informações sobre a transação.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_ CONV**</dt> <dt>0x40000000</dt> </dl>                | Uma conversa DDE foi estabelecida ou terminada. O objeto DDE contém uma estrutura [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) que fornece informações sobre a conversa.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ ERROS**</dt> <dt>0x10000000</dt> </dl>          | Ocorreu um erro de DDE. O objeto DDE contém uma estrutura [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) que fornece informações sobre o erro.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt> </dl>   | Um aplicativo DDE criado, liberado ou incrementado a contagem de uso de um identificador de cadeia de caracteres, ou um identificador de cadeia de caracteres foi liberado como resultado de uma chamada para a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . O objeto DDE contém uma estrutura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) que fornece informações sobre o identificador da cadeia de caracteres.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_**</dt> <dt>0X20000000</dt> de links </dl>             | Um aplicativo DDE iniciou ou interrompeu um loop de aviso. O objeto DDE contém uma estrutura [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) que fornece informações sobre o loop de aviso.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_**</dt> <dt>0X04000000</dt> de mensagens </dl>    | O sistema ou um aplicativo postou uma mensagem DDE. O objeto DDE contém uma estrutura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ SENDMSGS**</dt> <dt>0x02000000</dt> </dl>    | O sistema ou um aplicativo enviou uma mensagem DDE. O objeto DDE contém uma estrutura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que fornece informações sobre a mensagem.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função de retorno de chamada processar essa transação, ela deverá retornar 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



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

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

