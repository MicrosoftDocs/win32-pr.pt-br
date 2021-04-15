---
description: A função DocumentEvent é um manipulador de eventos para eventos associados à impressão de um documento.
ms.assetid: 1250116e-55c7-470f-97f6-36f27a31a841
title: Função DocumentEvent (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentEvent
- DocumentEventA
- DocumentEventW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aa80e5fe17047eceacdc30e2a40a4a629088d89f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505846"
---
# <a name="documentevent-function"></a>Função DocumentEvent

A função **DocumentEvent** é um manipulador de eventos para eventos associados à impressão de um documento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DocumentEvent(
  _In_  HANDLE hPrinter,
  _In_  HDC    hdc,
        INT    iEsc,
        ULONG  cbIn,
  _In_  PVOID  pvIn,
        ULONG  cbOut,
  _Out_ PVOID  pvOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para um objeto de impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*HDC* \[ no\]
</dt> <dd>

Um identificador de contexto de dispositivo que é gerado por uma chamada de [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Isso será zero se *iEsc* estiver definido como DOCUMENTEVENT \_ CREATEDCPRE. Para obter restrições sobre a impressão de um aplicativo de 32 bits em uma versão de 64 bits do Windows, consulte comentários.

</dd> <dt>

*iEsc* 
</dt> <dd>

Um código de escape que identifica o evento a ser manipulado. Esse parâmetro pode ser uma das seguintes constantes de inteiro.



| Constante                                                                                                                                                                                                                                                                                                                                               | Evento                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ AbortDoc**</dt> </dl>                                                                                                                                                               | O GDI está prestes a processar uma chamada para sua função [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | O GDI acabou de processar uma chamada para sua função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**createy**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/> Este código de escape não deve ser usado, a menos que tenha havido uma chamada anterior para **DocumentEvent** com *IESC* definido como DocumentEvent \_ CREATEDCPRE.<br/>                                 |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | O GDI está prestes a processar uma chamada para sua função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**createy**](/windows/desktop/api/wingdi/nf-wingdi-createica) .<br/>                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | O GDI está prestes a processar uma chamada para sua função [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | O GDI acabou de processar uma chamada para sua função [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                              |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ EndDoc**</dt> </dl>                 | O GDI está prestes a processar uma chamada para sua função [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .<br/>                                                                                                                                                                                                                             |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDpage**</dt> </dl>                                                                                                                                                                  | O GDI está prestes a processar uma chamada para sua função [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ escape**</dt> </dl>                                                                                                                                                                     | O GDI está prestes a processar uma chamada para sua função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .<br/>                                                                                                                                                                                                                       |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | O \_ evento DOCUMENTEVENT QUERYFILTER representa uma oportunidade para o spooler consultar o driver para obter uma lista dos eventos do DOCUMENTEVENT \_ *xxx* aos quais o driver responderá. Esse evento é emitido logo antes de uma chamada para **DocumentEvent** que passa o \_ evento DocumentEvent CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | O GDI acabou de processar uma chamada para sua função [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/> Este código de escape não deve ser usado, a menos que tenha havido uma chamada anterior para **DocumentEvent** com *IESC* definido como DocumentEvent \_ RESETDCPRE.<br/>                                                                    |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | O GDI está prestes a processar uma chamada para sua função [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) .<br/>                                                                                                                                                                                                                           |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | O GDI acabou de processar uma chamada para sua função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ StartDoc**</dt> </dl> | O GDI está prestes a processar uma chamada para sua função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ Startpage**</dt> </dl>                                                                                                                                                            | O GDI está prestes a processar uma chamada para sua função [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) .<br/>                                                                                                                                                                                                                       |



 

</dd> <dt>

*cbIn* 
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pvIn*.

</dd> <dt>

*pvIn* \[ no\]
</dt> <dd>

Um ponteiro para um buffer. O que o buffer contém depende do valor de *iEsc*, conforme mostrado na tabela a seguir.



| Constante                                                                                                                                                                                                                                                                                                                                               | Conteúdo do pvin                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_ABORTDOC"></span><span id="documentevent_abortdoc"></span><dl> <dt>**DOCUMENTEVENT \_ AbortDoc**</dt> </dl>                                                                                                                                                               | Não usado.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_CREATEDCPOST"></span><span id="documentevent_createdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* contém o endereço de um ponteiro para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada no parâmetro *pvOut* em uma chamada anterior para essa função, para a qual o parâmetro *iEsc* foi definido como DOCUMENTEVENT \_ CREATEDCPRE.<br/> |
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl>                                                                                                                                                      | *pvIn* aponta para uma estrutura de CREATEDCPRE de DOCEVENT, \_ que está documentada no [Kit de desenvolvimento de driver do Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                   |
| <span id="DOCUMENTEVENT_DELETEDC"></span><span id="documentevent_deletedc"></span><dl> <dt>**DOCUMENTEVENT \_ DELETEDC**</dt> </dl>                                                                                                                                                               | Não usado.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPOST"></span><span id="documentevent_enddocpost"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPOST**</dt> </dl>                                                                                                                                                         | Não usado.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDDOCPRE_or_DOCUMENTEVENT_ENDDOC"></span><span id="documentevent_enddocpre_or_documentevent_enddoc"></span><span id="DOCUMENTEVENT_ENDDOCPRE_OR_DOCUMENTEVENT_ENDDOC"></span><dl> <dt>**DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ EndDoc**</dt> </dl>                 | Não usado.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ENDPAGE"></span><span id="documentevent_endpage"></span><dl> <dt>**DOCUMENTEVENT \_ ENDpage**</dt> </dl>                                                                                                                                                                  | Não usado.<br/>                                                                                                                                                                                                                          |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ escape**</dt> </dl>                                                                                                                                                                     | *pvIn* aponta para uma estrutura de escape DOCEVENT, \_ que está documentada no [Kit de desenvolvimento de driver do Windows](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                                                        |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl>                                                                                                                                                      | O mesmo que para DOCUMENTEVENT \_ CREATEDCPRE.<br/>                                                                                                                                                                                            |
| <span id="DOCUMENTEVENT_RESETDCPOST"></span><span id="documentevent_resetdcpost"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPOST**</dt> </dl>                                                                                                                                                      | *pvIn* contém o endereço de um ponteiro para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada no parâmetro *pvOut* em uma chamada anterior para essa função, para a qual o parâmetro *iEsc* foi definido como DOCUMENTEVENT \_ RESETDCPRE.<br/>  |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>                                                                                                                                                         | *pvIn* contém o endereço de um ponteiro para a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornecida pelo chamador de [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTDOCPOST"></span><span id="documentevent_startdocpost"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPOST**</dt> </dl>                                                                                                                                                   | *pvIn* aponta para um longo que especifica o identificador do trabalho de impressão retornado por [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                                                          |
| <span id="DOCUMENTEVENT_STARTDOCPRE_or_DOCUMENTEVENT_STARTDOC"></span><span id="documentevent_startdocpre_or_documentevent_startdoc"></span><span id="DOCUMENTEVENT_STARTDOCPRE_OR_DOCUMENTEVENT_STARTDOC"></span><dl> <dt>**DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ StartDoc**</dt> </dl> | *pvIn* contém o endereço de um ponteiro para uma estrutura [**DOCINFO**](/windows/desktop/api/Wingdi/ns-wingdi-docinfoa) fornecida pelo chamador de [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).<br/>                                                                                         |
| <span id="DOCUMENTEVENT_STARTPAGE"></span><span id="documentevent_startpage"></span><dl> <dt>**DOCUMENTEVENT \_ Startpage**</dt> </dl>                                                                                                                                                            | Não usado.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>*cbOut*</dt> <dd> 

| Valor                       | Significado                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------|
| IDOCUMENTEVENT \_ QUERYFILTER | O tamanho, em bytes, do ponteiro de buffer para por *pvOut*.                             |
| DOCUMENTEVENT \_ escape       | Um valor que é usado como o parâmetro *cbOutput* para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). |
| Para todos os outros valores        | *iEsc* não é usado.                                                                  |



 

</dd> <dt>

*pvOut* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer. O conteúdo do buffer depende do valor fornecido para *iEsc*, conforme mostrado na tabela a seguir.



| Constante                                                                                                                                                                                          | Conteúdo do pvOut                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DOCUMENTEVENT_CREATEDCPRE"></span><span id="documentevent_createdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ CREATEDCPRE**</dt> </dl> | Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornecida por Driver, que o GDI usa em vez de um fornecido pelo chamador [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) . (Se **NULL**, GDI usa a estrutura fornecida pelo chamador.)<br/> |
| <span id="DOCUMENTEVENT_ESCAPE"></span><span id="documentevent_escape"></span><dl> <dt>**DOCUMENTEVENT \_ escape**</dt> </dl>                | Um ponteiro para um buffer que é usado como o parâmetro *lpszOutData* para [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).<br/>                                                                                                              |
| <span id="DOCUMENTEVENT_QUERYFILTER"></span><span id="documentevent_queryfilter"></span><dl> <dt>**DOCUMENTEVENT \_ QUERYFILTER**</dt> </dl> | Um ponteiro para o buffer que contém uma estrutura de filtro DOCEVENT, \_ documentada no [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428).<br/>                                          |
| <span id="DOCUMENTEVENT_RESETDCPRE"></span><span id="documentevent_resetdcpre"></span><dl> <dt>**DOCUMENTEVENT \_ RESETDCPRE**</dt> </dl>    | Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) fornecida por Driver, que o GDI usa em vez de um fornecido pelo chamador [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca) . (Se **NULL**, GDI usa a estrutura fornecida pelo chamador.)<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno da função depende do escape fornecido para *iEsc*. Para alguns códigos de escape, o valor de retorno não é usado (veja abaixo). Se a função fornecer um valor de retorno, ela deverá ser uma das opções a seguir.



| Valor Retornado               | Significado                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| falha de DOCUMENTEVENT \_     | O driver dá suporte ao código de escape identificado por *iEsc*, mas ocorreu uma falha. |
| DOCUMENTEVENT \_ êxito     | O driver tratou com êxito o código de escape identificado por *iEsc*.             |
| DOCUMENTEVENT \_ sem suporte | O driver não oferece suporte ao código de escape identificado por *iEsc*.                 |



 

A lista a seguir indica quais códigos de escape exigem um valor de retorno e quais não, e explica o significado do sucesso do DOCUMENTEVENT \_ , \_ falha DOCUMENTEVENT e \_ códigos de retorno sem suporte do DOCUMENTEVENT.



| Valor Retornado                                          | Significado                                                                                                                                                                                    |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ AbortDoc                               | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPOST                           | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ CREATEDCPRE                            | DOCUMENTEVENT \_ Failure-GDI não cria o contexto do dispositivo ou o contexto de informações e fornece um valor de retorno de 0 para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**createy**](/windows/desktop/api/wingdi/nf-wingdi-createica). |
| DOCUMENTEVENT \_ DELETEDC                               | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPOST                             | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDDOCPRE ou DOCUMENTEVENT \_ EndDoc     | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ ENDpage                                | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ escape                                 | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ QUERYFILTER                            | Consulte Observações.                                                                                                                                                                               |
| DOCUMENTEVENT \_ RESETDCPOST                            | O valor de retorno não é usado e não deve ser lido.                                                                                                                                       |
| DOCUMENTEVENT \_ RESETDCPRE                             | DOCUMENTEVENT \_ Failure-GDI não redefine o contexto do dispositivo e fornece um valor de retorno de 0 para [**ResetDC**](/windows/desktop/api/wingdi/nf-wingdi-resetdca).                                                           |
| DOCUMENTEVENT \_ STARTDOCPOST                           | DOCUMENTEVENT \_ Failure-GDI chama [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc) para parar o documento e, em seguida, fornece um valor de retorno de erro de SP \_ para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                      |
| DOCUMENTEVENT \_ STARTDOCPRE ou DOCUMENTEVENT \_ StartDoc | Falha de DOCUMENTEVENT \_ -GDI não inicia o documento e fornece um valor de retorno de erro de SP \_ para [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).                                                       |
| DOCUMENTEVENT \_ Startpage                              | Falha de DOCUMENTEVENT \_ -GDI não inicia a página e fornece um valor de retorno de erro de SP \_ para [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage).                                                         |



 

## <a name="remarks"></a>Comentários

Para um valor *iEsc* de DOCUMENTEVENT \_ QUERYFILTER, o spooler pode interpretar um valor de \_ êxito DOCUMENTEVENT retornado por **DOCUMENTEVENT** de duas maneiras, dependendo se o driver modificou determinados membros da \_ estrutura de filtro DOCEVENT (que está documentada no [Windows Driver Development Kit](https://msdn.microsoft.com/windows/hardware/gg487428) ). (O parâmetro *pvOut* aponta para essa estrutura.) Quando o spooler aloca memória para uma estrutura desse tipo, ele inicializa dois membros dessa estrutura, **cElementsReturned** e **cElementsNeeded**, para valores conhecidos. Após o retorno de **DocumentEvent** , o spooler determina se os valores desses membros foram alterados e usa essas informações para interpretar o valor de retorno de **DocumentEvent** . A tabela a seguir resume essa situação.



| Valor Retornado                          | Status de cElementsReturned e cElementsNeeded    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOCUMENTEVENT \_ êxito<br/>     | O driver não fez nenhuma alteração em nenhum dos membros.<br/> | O spooler interpreta esse valor de retorno como equivalente a DOCUMENTEVENT \_ sem suporte. O spooler não pode recuperar o filtro de eventos do driver, portanto, ele persiste na chamada de **DocumentEvent** para todos os eventos.<br/>                                                                                                                                                                                                                         |
| DOCUMENTEVENT \_ êxito<br/>     | O driver gravou em um ou em ambos os membros.<br/>    | O spooler aceita esse valor de retorno sem interpretação. Se o driver gravar apenas um de **cElementsNeeded** e **cElementsReturned**, o spooler considerará que o membro inalterado tem um valor igual a zero.<br/> O spooler filtra todos os eventos listados no membro **aDocEventCall** do \_ filtro DOCEVENT (que está documentado no kit de [desenvolvimento de driver do Windows](https://msdn.microsoft.com/windows/hardware/gg487428) ).<br/> |
| DOCUMENTEVENT \_ sem suporte<br/> | Não aplicável<br/>                          | O driver não dá suporte a DOCUMENTEVENT \_ QUERYFILTER.<br/> O spooler não pode recuperar o filtro de eventos do driver, portanto, ele persiste na chamada de **DocumentEvent** para todos os eventos.<br/>                                                                                                                                                                                                                                            |
| falha de DOCUMENTEVENT \_<br/>     | Não aplicável<br/>                          | O driver dá suporte a DOCUMENTEVENT \_ QUERYFILTER, mas encontrou um erro interno.<br/> O spooler não pode recuperar o filtro de eventos do driver, portanto, ele persiste na chamada de **DocumentEvent** para todos os eventos.<br/>                                                                                                                                                                                                                 |



 

Se o código de escape fornecido no parâmetro *iEsc* for DOCUMENTEVENT \_ CREATEDCPRE, as seguintes regras se aplicarão:

-   Se o trabalho estiver sendo enviado diretamente para a impressora sem spool, pvIn->pszDevice aponta para o nome da impressora. (Para obter mais informações, consulte a documentação do DOCEVENT \_ Estrutura CREATEDCPRE no [Kit de desenvolvimento de driver do Windows](https://msdn.microsoft.com/windows/hardware/gg487428).)
-   Se o trabalho estiver sendo colocado no spool, pvIn->pszDevice aponta para o nome da porta da impressora.

> [!Note]  
> As seguintes restrições se aplicam ao executar um aplicativo de 32 bits em uma versão de 64 bits do Windows. A única função GDI que **DocumentEvent** deve chamar é [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape), e somente os escapes privados devem ser usados. Chamadas **DocumentEvent** para outras funções GDI podem produzir comportamento indefinido.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DocumentEventW** (Unicode) e **DocumentEventA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[Kit de desenvolvimento de driver do Windows](https://msdn.microsoft.com/windows/hardware/gg487428)
</dt> </dl>

 

