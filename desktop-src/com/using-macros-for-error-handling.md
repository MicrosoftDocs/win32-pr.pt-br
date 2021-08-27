---
title: Usando macros para tratamento de erro
description: COM define um número de macros que facilitam o trabalho com valores HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480532"
---
# <a name="using-macros-for-error-handling"></a>Usando macros para tratamento de erro

COM define um número de macros que facilitam o trabalho com valores **HRESULT** .

As macros de tratamento de erros são descritas na tabela a seguir.




| Macro | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Retorna um <strong>HRESULT</strong> dado o bit de severidade, o código de recurso e o código de erro que compõem o <strong>HRESULT</strong>.<br /><blockquote>[!Note]<br />Chamar <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> para verificação de S_OK transporta uma penalidade de desempenho. Você não deve usar rotineiramente <strong>MAKE_HRESULT</strong> para resultados bem-sucedidos.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Retorna um <strong>SCODE</strong> dado o bit de severidade, o código de recurso e o código de erro que compõem o <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Extrai a parte do código de erro do <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Extrai o código de recurso do <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Extrai o bit de severidade do <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Extrai a parte do código de erro do <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Extrai o código de recurso do <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Extrai o campo de severidade do <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>FOI</strong></a><br /> | Testa o bit de severidade do <strong>SCODE</strong> ou <strong>HRESULT</strong>; retornará <strong>true</strong> se a severidade for zero e <strong>false</strong> se for uma.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>Falha ao</strong></a><br /> | Testa o bit de severidade do <strong>SCODE</strong> ou <strong>HRESULT</strong>; retornará <strong>true</strong> se a severidade for um e <strong>false</strong> se for zero.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Fornece um teste genérico para erros em qualquer valor de status. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Mapas um <a href="/windows/desktop/Debug/system-error-codes">código de erro do sistema</a> para um valor <strong>HRESULT</strong> . <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Mapas um valor de status do NT para um valor <strong>HRESULT</strong> .<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

