---
description: Solicitações para executar a análise offline com a origem, o manifesto, os parâmetros e o quadro especificado.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IOfflineAnalysisRequest::RequestOfflineAnalysisAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85243b1c07db1f2c30a4e29b221582fd507360f1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624332"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Método IOfflineAnalysisRequest::RequestOfflineAnalysisAsync

Solicitações para executar a análise offline com a origem, o manifesto, os parâmetros e o quadro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a>Parâmetros

*analysisSource*   
Especifica de onde a fonte de análise vem de relatórios armazenados em cache ou de reprodução.

*manifestXml*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo de manifesto XML.

*parametersXml*   
Uma cadeia de caracteres COM que contém o nome do caminho do arquivo de parâmetros XML.

*Cookie*   
Um cookie que identifica exclusivamente a solicitação e pode ser usado para sinalizar para que ela seja cancelada.

*captureFullFileName*   
Uma cadeia de caracteres COM que contém o nome de caminho absoluto do arquivo de captura (.vsglog).

*frameNumber*   
O quadro especificado.

*outputFullFileName*   
Uma cadeia de caracteres COM que contém o nome de caminho absoluto do arquivo em que a saída é escrita.

*requestCallback*   
O endereço de um retorno de chamada usado para notificar o host dos resultados.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
