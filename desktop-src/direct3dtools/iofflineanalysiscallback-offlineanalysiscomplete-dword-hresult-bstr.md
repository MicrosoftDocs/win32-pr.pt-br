---
description: Uma função de retorno de chamada usada para notificar o host que a análise offline foi concluída.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IOfflineAnalysisCallback:: OfflineAnalysisComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a1ece7106bee1c49f97238bf06348b049d3f7167
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500721"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>Método IOfflineAnalysisCallback:: OfflineAnalysisComplete

Uma função de retorno de chamada usada para notificar o host que a análise offline foi concluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a>Parâmetros

*cookie*   
Um cookie que identifica exclusivamente a solicitação que iniciou a análise offline.

*disso*   
Indica se a análise offline foi bem-sucedida ou falhou. Se tiver êxito, os resultados foram gravados em um arquivo.

*outputFullFileName*   
Uma cadeia de caracteres COM contianing o nome do arquivo onde os resultados da análise offline foram gravados.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IOfflineAnalysisCallback**](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
