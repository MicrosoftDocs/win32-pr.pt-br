---
description: A função PdhVbGetOneCounterPath exibe uma caixa de diálogo que permite que o usuário procure os contadores de desempenho disponíveis e selecione um contador.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Função PdhVbGetOneCounterPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: da6cc5b476373a55135d91d21163f15cb04379fff9d7c7c2cf1342451a5a201d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061154"
---
# <a name="pdhvbgetonecounterpath-function"></a>Função PdhVbGetOneCounterPath

A **função PdhVbGetOneCounterPath** exibe uma caixa de diálogo que permite que o usuário procure os contadores de desempenho disponíveis e selecione um contador. O contador selecionado é retornado na *variável PathString.* A *variável PathString* deve ser dimensionada e inicializada antes que essa função seja chamada e o tamanho dimensionado deve ser indicado pela *variável PathLength.*

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [Funções de Contadores de Desempenho](performance-counters-functions.md).

Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PathString* 
</dt> <dd>

Variável de cadeia de caracteres inicializada usada para receber o caminho do contador selecionado pelo usuário.

</dd> <dt>

*PathLength* 
</dt> <dd>

Comprimento da PathString inicializada.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores a serem exibidos na caixa de diálogo. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**DETALHES DE PERF \_ \_ AVANÇADOS**</dt> </dl> | Contadores que o usuário avançado provavelmente entenderá, além dos contadores de usuário iniciante.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**PERF \_ DETAIL \_ EXPERT**</dt> </dl>       | Contadores que o usuário especialista e o desenvolvedor de software provavelmente entenderão, além dos contadores para usuários iniciantes e avançados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**\_NOVICE DE DETALHES DE \_ PERF**</dt> </dl>       | Somente contadores que o usuário iniciante provavelmente entenderá.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**ASSISTENTE DE \_ DETALHES DE \_ PERF**</dt> </dl>       | Todos os contadores no sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variável de cadeia de caracteres que contém o texto que será exibido na barra de legendas da caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna o número de caracteres gravados no buffer *PathString.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




