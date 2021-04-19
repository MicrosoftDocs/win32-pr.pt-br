---
title: Códigos de erro do WER (Werapi. h)
description: A tabela a seguir fornece uma lista de códigos de erro personalizados usados pelo Relatório de Erros do Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781309"
---
# <a name="wer-error-codes"></a>Códigos de erro do WER

A tabela a seguir fornece uma lista de códigos de erro personalizados usados pelo Relatório de Erros do Windows.



| Constante                                                                                                                                                                                            | Descrição                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <dt>**WER \_ E \_ buffer insuficiente \_**</dt> </dl> | Um buffer é muito pequeno para conter os dados.<br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <dt>**WER \_ E \_ \_ estado inválido**</dt> </dl>                   | Uma função foi chamada de uma maneira sem suporte.<br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <dt>**WER \_ E \_ comprimento \_ excedidos**</dt> </dl>             | Um dos limites de comprimento foi excedido.<br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <dt>**parâmetro do WER \_ E \_ ausente \_**</dt> </dl>                   | Um ou mais parâmetros estão ausentes.<br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <dt>**WER \_ E \_ não \_ encontrado**</dt> </dl>                               | Elemento não encontrado.<br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <dt>**repositório do WER \_ E \_ \_ desabilitado**</dt> </dl>                | O repositório foi desabilitado.<br/>                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Werapi. h</dt> </dl> |



 

 





