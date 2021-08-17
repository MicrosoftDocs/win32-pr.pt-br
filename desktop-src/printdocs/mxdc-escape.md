---
description: A \_ função de escape de impressora de escape MXDC permite que os aplicativos gravem documentos em um arquivo ou em uma impressora no formato XPS (XML Paper Specification) por meio do MXDC (Microsoft XPS Document Converter).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: Função MXDC_ESCAPE (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7ace79404808db750a15b2c17b6fedb336dbd1d72b1581888324a4d87bb7cd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460876"
---
# <a name="mxdc_escape-function"></a>\_Função de escape MXDC

A função de escape de impressora de **\_ escape MXDC** permite que os aplicativos gravem documentos em um arquivo ou em uma impressora no formato XPS (XML Paper Specification) por meio do MXDC (Microsoft XPS Document Converter).

Para executar essa operação, chame a função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com os parâmetros a seguir.

## <a name="syntax"></a>Sintaxe


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* 
</dt> <dd>

Um identificador para o contexto do dispositivo de impressora.

</dd> <dt>

*cbInput* 
</dt> <dd>

O tamanho, em bytes, dos dados apontados pelo parâmetro *lpszInData* .

</dd> <dt>

*lpszInData* 
</dt> <dd>

Um ponteiro para um buffer que contém os dados de entrada, que são sempre armazenados em uma das estruturas a seguir.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Cada uma dessas estruturas tem um membro opcode que especifica o que o MXDC deve fazer. Consulte MxdcEscapeHeader para comentários detalhados sobre esses códigos.



| Código de operações (opcode)                                                                                                                                                                                                  | Ação                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ obter \_ nome de arquivo**</dt> </dl>                                          | Define o parâmetro *lpszOutData* da função [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) como, o caminho completo do arquivo de saída como uma cadeia de caracteres terminada em zero ou o tamanho dessa cadeia de caracteres.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**\_Seq de \_ \_ Doc fixo \_ do MXDCOP PRINTTICKET**</dt> </dl> | Associa um tíquete de impressão a uma sequência de documento fixa XPS.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**\_ \_ Doc fixo do MXDCOP PRINTTICKET \_**</dt> </dl>              | Associa um tíquete de impressão a um documento XPS.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**\_ \_ página fixa do MXDCOP PRINTTICKET \_**</dt> </dl>           | Associa um tíquete de impressão a uma página XPS.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ set \_ S0PAGE**</dt> </dl>                                                | Envia a marcação XPS da página atual para a saída.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**MXDCOP \_ definir \_ \_ recurso S0PAGE**</dt> </dl>                    | Envia um recurso na página, como uma imagem ou fonte, para a saída.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ definir \_ \_ modo XPSPASSTHRU**</dt> </dl>                 | Coloca o MXDC em um estado de passagem, permitindo que um aplicativo grave o XPS diretamente no arquivo de saída sem nenhum processamento pelo MXDC. Um documento inteiro ou até mesmo uma sequência de documento pode ser escrito dessa maneira.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

O tamanho, em bytes, dos dados apontados pelo parâmetro *lpszOutData* .

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Um ponteiro para um buffer que contém os dados de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será maior que zero. Se a função falhar ou não tiver suporte, o valor de retorno será menor ou igual a zero.

## <a name="remarks"></a>Comentários

Esse escape é suportado por MXDC e XPSDrv, mas não pela GDI.

Para determinar se o driver de impressora é o MXDC, chame [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) com o escape [**gettechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Se o driver for o MXDC, o **ExtEscape** retornará a cadeia de caracteres com terminação zero, " http://schemas.microsoft.com/xps/2005/06 ". Verifique se o buffer referenciado pelo parâmetro *lpszOutData* é grande o suficiente para conter essa cadeia de caracteres.

para determinar se o driver de impressora é o Windows driver de gravador de documento xps da microsoft, confirme se o driver de impressora é o MXDC e, em seguida, determine se o nome do driver de impressora é "Microsoft xps Document writer".

Para obter o nome do driver de impressora, use uma das técnicas a seguir. <dl> Chame [**GetPrinterDriver**](getprinterdriver.md) com o valor do parâmetro *Level* definido como 1. O nome do driver de impressora é retornado no membro **pname** da [**estrutura \_ info \_ do driver 1**](driver-info-1.md) .  
ou  
Chame [**Getprinter**](getprinter.md) com o valor do parâmetro *Level* definido como 2. O nome do driver de impressora é retornado no membro **pDriverName** da [**estrutura \_ info \_ 2 da impressora**](printer-info-2.md) .  
</dl>

A tabela a seguir mostra onde encontrar vários objetos no arquivo XPS que vários tipos de objetos serão gravados.



| Objeto       | Local no arquivo de saída    |
|--------------|--------------------------------|
| Página fixa   | /Documents/1/Pages/Esc%d.fpage |
| Thumbnail    | /Documents/1/Metadata          |
| Tíquete de impressão | /Documents/1/Metadata          |
| Fonte         | /Documents/1/Resources/Fonts   |
| Imagem        | /Documents/1/Resources/Images  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções de escape de impressora](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

