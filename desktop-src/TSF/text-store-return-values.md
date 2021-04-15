---
title: Valores de retorno do repositório de texto (Textstor. h)
description: Quando um Gerenciador de documentos processa um armazenamento de texto, ele produz valores de retorno no intervalo de 0xHHHH0200 a 0xHHHH0300. A tabela a seguir lista os valores de retorno de armazenamento de texto em ordem alfabética.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499582"
---
# <a name="text-store-return-values"></a>Valores de retorno do repositório de texto

Quando um Gerenciador de documentos processa um armazenamento de texto, ele produz valores de retorno no intervalo de 0x *HHHH* 0200 a 0x *HHHH* 0300. A tabela a seguir lista os valores de retorno de armazenamento de texto em ordem alfabética.



| Código/valor de retorno                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_ \_Formato E**</dt> <dt>0x8004020a</dt> </dl>                   | O aplicativo não dá suporte ao tipo de dados contido no objeto [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) a ser inserido usando [**ITextStoreACP:: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl> | O parâmetro não está dentro da caixa delimitadora de qualquer caractere.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>       | O intervalo especificado se estende para fora do documento.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>    | O objeto não oferece suporte à interface solicitada.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_ E \_ nolayout**</dt> <dt>0x80040206</dt> </dl>             | O aplicativo não calculou um layout de texto.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                   | O aplicativo não tem um bloqueio somente leitura ou um bloqueio de leitura/gravação para o documento.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_ 0x80040202 \_ NOobject**</dt> <dt></dt> </dl>             | O deslocamento de conteúdo inserido não está posicionado antes de um caractere de TF \_ Char \_ inserido.<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_ E \_ NOselecting**</dt> <dt>0x80040205</dt> </dl>    | O documento não tem seleção.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_ E \_ noservice**</dt> <dt>0x80040203</dt> </dl>          | O conteúdo não pode ser retornado para corresponder ao GUID do serviço.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_ E \_ ReadOnly**</dt> <dt>0x80040209</dt> </dl>             | O documento é somente leitura. Não é possível modificar o conteúdo.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_ E \_**</dt> <dt>0x00040300</dt> síncrono </dl>    | O documento não pode ser bloqueado de forma síncrona.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_ S \_ Async**</dt> <dt>(0x1)</dt> </dl>                         | O documento recebeu com êxito um bloqueio assíncrono.<br/>                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITextStoreACP:: InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

