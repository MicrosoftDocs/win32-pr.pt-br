---
title: Valores de retorno do gerente (Msctf.h)
description: O Estrutura de Serviços de Texto produz valores de retorno no intervalo de 0xHHHH0200 a 0xH OH0507. A tabela a seguir fornece ao gerente valores de retorno em ordem alfabética.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9e914e393a136205a0e1bb3338c43c4cbb6a9dbaf75dad43255eeac2f999f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876671"
---
# <a name="manager-return-values"></a>Valores de retorno do gerente

O Estrutura de Serviços de Texto produz valores de retorno no intervalo de 0x *H OH* 0200 a 0x *H OH* 0507. A tabela a seguir fornece ao gerente valores de retorno em ordem alfabética.

> [!Note]  
> As descrições fornecidas são não específicas; o significado de um valor retornado pode variar dependendo do método que retornou o valor.

 



| Valor/código de retorno                                                                                                                                                                                                                                                   | Descrição                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**TF \_ E \_ JÁ \_ EXISTE**</dt> <dt>0X80040506</dt> </dl>                   | A chave preservada é registrada.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**TF \_ E \_ COMPOSITION \_ REJECTED**</dt> <dt>0X80040508</dt> </dl> | O proprietário do contexto rejeitou a composição.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**TF \_ E \_ DISCONNECTED**</dt> <dt>0X80040504</dt> </dl>                          | O objeto de contexto não está em uma pilha de documentos.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**TF \_ E \_ EMPTYCONTEXT**</dt> <dt>0x80040509</dt> </dl>                          | O contexto está vazio.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**TF \_ E \_ FORMAT**</dt> <dt>0x8004020a</dt> </dl>                                            | O proprietário do contexto não pode manipular objetos do tipo fornecido pelo parâmetro pDataObject.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**TF \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl>                          | As coordenadas da tela são inválidas.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**TF \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>                                | A posição do caractere é inválida.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**TF \_ E \_ INVALIDVIEW**</dt> <dt>0x80040505</dt> </dl>                             | A exibição de contexto é inválida.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**TF \_ E \_ LOCKED**</dt> <dt>0x80040500</dt> </dl>                                            | O contexto já está bloqueado.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**TF \_ E \_ NOINTERFACE**</dt> <dt>0x80040204</dt> </dl>                             | O objeto não dá suporte à interface solicitada.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**TF \_ E \_ NOLAYOUT**</dt> <dt>0x80040206</dt> </dl>                                      | O layout de texto não foi calculado.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**TF \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                                            | O chamador não tem o tipo de documento necessário.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**TF \_ E \_ NOOBJECT**</dt> <dt>0x80040202</dt> </dl>                                      | Nenhum objeto inserido existe na posição especificada.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**TF \_ E \_ NOPROVIDER**</dt> <dt>0x80040503</dt> </dl>                                | Não existe nenhum provedor de funções para a função especificada.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**TF \_ E \_ NOSELECTION**</dt> <dt>0x80040205</dt> </dl>                             | Não existe nenhuma seleção dentro do contexto.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**TF \_ E \_ NOSERVICE**</dt> <dt>0x80040203</dt> </dl>                                   | O serviço especificado não existe ou não pode ser criado.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**TF \_ E \_ NORANGEEDRANGE**</dt> <dt>0x80040502</dt> </dl>                       | O gerenciador do TSF não possui o intervalo.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**TF \_ INTERVALO E \_ \_ NÃO COBERTO \_ 0X80040507**</dt> <dt></dt> </dl>         | O intervalo não está dentro de uma composição ativa.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**TF \_ E \_ READONLY**</dt> <dt>0x80040209</dt> </dl>                                      | O contexto de edição é somente leitura.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**TF \_ E \_ STACKFULL**</dt> <dt>0x80040501</dt> </dl>                                   | A pilha de contexto está cheia.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**TF \_ E \_ SÍNCRONO**</dt> <dt>0x80040208</dt> </dl>                             | Não é possível obter um bloqueio síncrono somente leitura.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**TF \_ S \_ ASYNC**</dt> <dt>0x00040300</dt> </dl>                                               | Os dados serão obtidos de forma assíncrona.<br/>                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                      |
| Cabeçalho<br/>                   | <dl> <dt>Msctf.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msctf.idl</dt> </dl> |



 

 





