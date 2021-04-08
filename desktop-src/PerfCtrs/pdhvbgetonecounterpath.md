---
description: A função PdhVbGetOneCounterPath exibe uma caixa de diálogo que permite ao usuário procurar os contadores de desempenho disponíveis e selecionar um contador.
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
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828386"
---
# <a name="pdhvbgetonecounterpath-function"></a>Função PdhVbGetOneCounterPath

A função **PdhVbGetOneCounterPath** exibe uma caixa de diálogo que permite ao usuário procurar os contadores de desempenho disponíveis e selecionar um contador. O contador selecionado é retornado na variável *pathstring* . A variável *pathstring* deve ser dimensionada e inicializada antes que essa função seja chamada, e o tamanho de dimensão deve ser indicado pela variável *PathLength* .

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbGetOneCounterPath ( \_ ByVal caminhostring como cadeia de caracteres, \_ ByVal PathLength como longo, \_ ByVal DetailLevel como Long, \_ ByVal legendastring as String \_ ) como longo

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho da* 
</dt> <dd>

Variável de cadeia de caracteres inicializada usada para receber o caminho do contador selecionado pelo usuário.

</dd> <dt>

*PathLength* 
</dt> <dd>

Comprimento do Caminhostring inicializado.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores a serem exibidos na caixa de diálogo. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**detalhes do desempenho \_ \_ avançado**</dt> </dl> | Os contadores que o usuário avançado provavelmente entenderá, além dos contadores de usuário iniciantes.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**\_especialista em detalhes de desempenho \_**</dt> </dl>       | Os contadores que o usuário experiente e o desenvolvedor de software provavelmente compreenderão, além dos contadores para os usuários iniciantes e avançados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**reiniciante de detalhes de desempenho \_ \_**</dt> </dl>       | Somente os contadores que o usuário iniciante provavelmente entenderá.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**\_Assistente de detalhes de desempenho \_**</dt> </dl>       | Todos os contadores no sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*Legendastring* 
</dt> <dd>

Variável de cadeia de caracteres que contém o texto que será exibido na barra de legenda da caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o número de caracteres gravados no buffer *pathstring* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




